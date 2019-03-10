# hello-world
clear all;
close all;
clc;
screens = Screen('Screens');
screenNumber = max(screens);
black = BlackIndex(screenNumber);
white = WhiteIndex(screenNumber);
grey = white / 2;
[window, windowRect] = PsychImaging('OpenWindow', screenNumber, black);
Screen('BlendFunction', window, 'GL_SRC_ALPHA', 'GL_ONE_MINUS_SRC_ALPHA');
[screenXpixels, screenYpixels] = Screen('WindowSize', window);
Screen('TextSize', window, 80);
Screen('TextFont', window, 'Courier');
DrawFormattedText(window, 'Hello World', 'center', 'center', white);
Screen('Flip', window);
WaitSecs(5);
sca;
