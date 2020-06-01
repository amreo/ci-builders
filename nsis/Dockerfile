FROM fedora:30
RUN dnf install -y mingw32-nsis.x86_64
COPY SimpleSC.dll /usr/share/nsis/Plugins/x86-ansi/SimpleSC.dll
COPY SimpleSC.dll /usr/share/nsis/Plugins/x86-unicode/SimpleSC.dll
