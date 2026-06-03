Статическая библиотека и тест

cl /c /EHsc /std:c++17 /DLAB3_STATIC chesspiece.cpp slidingpiece.cpp jumpingpiece.cpp rook.cpp bishop.cpp queen.cpp horse.cpp king.cpp
lib /OUT:lab3_static.lib chesspiece.obj slidingpiece.obj jumpingpiece.obj rook.obj bishop.obj queen.obj horse.obj king.obj
cl /EHsc /std:c++17 /DLAB3_STATIC main.cpp lab3_static.lib /Fe:test_static.exe
Динамическая библиотека и тест

cl /LD /EHsc /std:c++17 /DLAB3_EXPORTS chesspiece.cpp slidingpiece.cpp jumpingpiece.cpp rook.cpp bishop.cpp queen.cpp horse.cpp king.cpp /Fe:lab3.dll
cl /EHsc /std:c++17 main.cpp lab3.lib /Fe:test_dynamic.exe

test_static.exe
test_dynamic.exe
