---
title: Types de données Windows (BaseTsd.h)
description: Les types de données pris en charge par Windows sont utilisés pour définir les valeurs de retour de fonction, les paramètres de fonction et de message, ainsi que les membres de structure.
ms.assetid: 4553cafc-450e-4493-a4d4-cb6e2f274d46
keywords:
- types de données
- types de données, fenêtres
- API Windows
- API Windows, types de données
- APIENTRY
- ATOM
- BOOL
- BOOLEAN
- BYTE
- RAPPEL
- CCHAR
- CHAR
- COLORREF
- CONST
- DWORD
- DWORDLONG
- DWORD_PTR
- DWORD32
- DWORD64
- FLOAT
- HACCEL
- HALF_PTR
- HANDLE
- HBITMAP
- HBRUSH
- HCOLORSPACE
- HCONV
- HCONVLIST
- HCURSOR
- HDC
- HDDEDATA
- HDESK
- HDROP
- HDWP
- HENHMETAFILE
- HFILE
- HFONT
- HGDIOBJ
- HGLOBAL
- HHOOK
- HICON
- HINSTANCE
- HKEY
- HKL
- HLOCAL
- HMENU
- HMETAFILE
- HMODULE
- HMONITOR
- HPALETTE
- HPEN
- HRESULT
- HRGN
- HRSRC
- HSZ
- HWINSTA
- HWND
- INT
- INT_PTR
- INT8
- INT16
- INT32
- INT64
- LANGID
- LCID
- LCTYPE
- LGRPID
- LONG
- LONGLONG
- LONG_PTR
- LONG32
- LONG64
- LPARAM
- LPBOOL
- LPBYTE
- LPCOLORREF
- LPCSTR
- LPCTSTR
- LPCVOID
- LPCWSTR
- LPDWORD
- LPHANDLE
- LPINT
- LPLONG
- LPSTR
- LPTSTR
- LPVOID
- LPWORD
- LPWSTR
- LRESULT
- PBOOL
- PBOOLEAN
- PBYTE
- PCHAR
- PCSTR
- PCTSTR
- PCWSTR
- PDWORD
- PDWORDLONG
- PDWORD_PTR
- PDWORD32
- PDWORD64
- PFLOAT
- PHALF_PTR
- PHANDLE
- PHKEY
- VIENNENT
- PINT_PTR
- PINT8
- PINT16
- PINT32
- PINT64
- PLCID
- PLONG
- PLONGLONG
- PLONG_PTR
- PLONG32
- PLONG64
- POINTER_32
- POINTER_64
- POINTER_SIGNED
- POINTER_UNSIGNED
- PSHORT
- PSIZE_T
- PSSIZE_T
- PSTR
- PTBYTE
- PTCHAR
- PTSTR
- PUCHAR
- PUHALF_PTR
- PUINT
- PUINT_PTR
- PUINT8
- PUINT16
- PUINT32
- PUINT64
- PULONG
- PULONGLONG
- PULONG_PTR
- PULONG32
- PULONG64
- PUSHORT
- DÉSIGNE
- PWCHAR
- PWORD
- PWSTR
- QWORD
- SC_HANDLE
- SC_LOCK
- SERVICE_STATUS_HANDLE
- SHORT
- SIZE_T
- SSIZE_T
- TBYTE
- TCHAR
- UCHAR
- UHALF_PTR
- UINT
- UINT_PTR
- DESTINÉES
- UINT16
- UINT32
- UINT64
- ULONG
- ULONGLONG
- ULONG_PTR
- ULONG32
- ULONG64
- UNICODE_STRING
- USHORT
- USN
- NULLITÉ
- WCHAR
- WINAPI
- WORD
- WPARAM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf3a23e816a78f0dcae9c2fbd6e6979b936451c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384524"
---
# <a name="windows-data-types"></a><span data-ttu-id="d6ac8-280">Types de données Windows</span><span class="sxs-lookup"><span data-stu-id="d6ac8-280">Windows Data Types</span></span>

<span data-ttu-id="d6ac8-281">Les types de données pris en charge par Windows sont utilisés pour définir les valeurs de retour de fonction, les paramètres de fonction et de message, ainsi que les membres de structure.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-281">The data types supported by Windows are used to define function return values, function and message parameters, and structure members.</span></span> <span data-ttu-id="d6ac8-282">Ils définissent la taille et la signification de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-282">They define the size and meaning of these elements.</span></span> <span data-ttu-id="d6ac8-283">Pour plus d’informations sur les types de données C/C++ sous-jacents, consultez [plages de types de données](/cpp/cpp/data-type-ranges?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="d6ac8-283">For more information about the underlying C/C++ data types, see [Data Type Ranges](/cpp/cpp/data-type-ranges?view=vs-2019).</span></span>

<span data-ttu-id="d6ac8-284">Le tableau suivant contient les types suivants : caractère, entier, booléen, pointeur et handle.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-284">The following table contains the following types: character, integer, Boolean, pointer, and handle.</span></span> <span data-ttu-id="d6ac8-285">Les types caractère, entier et booléen sont communs à la plupart des compilateurs C.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-285">The character, integer, and Boolean types are common to most C compilers.</span></span> <span data-ttu-id="d6ac8-286">La plupart des noms de type pointeur commencent par le préfixe P ou LP.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-286">Most of the pointer-type names begin with a prefix of P or LP.</span></span> <span data-ttu-id="d6ac8-287">Les handles font référence à une ressource qui a été chargée en mémoire.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-287">Handles refer to a resource that has been loaded into memory.</span></span>

<span data-ttu-id="d6ac8-288">Pour plus d’informations sur la gestion des entiers 64 bits, consultez [entiers volumineux](large-integers.md).</span><span class="sxs-lookup"><span data-stu-id="d6ac8-288">For more information about handling 64-bit integers, see [Large Integers](large-integers.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-289">Type de données</span><span class="sxs-lookup"><span data-stu-id="d6ac8-289">Data type</span></span></th>
<th><span data-ttu-id="d6ac8-290">Description</span><span class="sxs-lookup"><span data-stu-id="d6ac8-290">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d6ac8-291"><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-291"><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></span></span></td>
<td><span data-ttu-id="d6ac8-292">Convention d’appel pour les fonctions système.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-292">The calling convention for system functions.</span></span><br/> <span data-ttu-id="d6ac8-293">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-293">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define APIENTRY WINAPI</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-294"><span id="ATOM"></span><span id="atom"></span><strong>ATOM</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-294"><span id="ATOM"></span><span id="atom"></span><strong>ATOM</strong></span></span></td>
<td><span data-ttu-id="d6ac8-295">Atom.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-295">An atom.</span></span> <span data-ttu-id="d6ac8-296">Pour plus d’informations, consultez <a href="/windows/desktop/dataxchg/about-atom-tables">à propos des tables Atom</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-296">For more information, see <a href="/windows/desktop/dataxchg/about-atom-tables">About Atom Tables</a>.</span></span><br/> <span data-ttu-id="d6ac8-297">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-297">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef WORD ATOM;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-298"><span id="BOOL"></span><span id="bool"></span><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-298"><span id="BOOL"></span><span id="bool"></span><strong>BOOL</strong></span></span></td>
<td><span data-ttu-id="d6ac8-299">Variable booléenne (doit avoir la <strong>valeur true</strong> ou <strong>false</strong>).</span><span class="sxs-lookup"><span data-stu-id="d6ac8-299">A Boolean variable (should be <strong>TRUE</strong> or <strong>FALSE</strong>).</span></span><br/> <span data-ttu-id="d6ac8-300">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-300">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef int BOOL;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-301"><span id="BOOLEAN"></span><span id="boolean"></span><strong>EXPRESSION</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-301"><span id="BOOLEAN"></span><span id="boolean"></span><strong>BOOLEAN</strong></span></span></td>
<td><span data-ttu-id="d6ac8-302">Variable booléenne (doit avoir la <strong>valeur true</strong> ou <strong>false</strong>).</span><span class="sxs-lookup"><span data-stu-id="d6ac8-302">A Boolean variable (should be <strong>TRUE</strong> or <strong>FALSE</strong>).</span></span><br/> <span data-ttu-id="d6ac8-303">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-303">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef BYTE BOOLEAN;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-304"><span id="BYTE"></span><span id="byte"></span><strong>POIDS</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-304"><span id="BYTE"></span><span id="byte"></span><strong>BYTE</strong></span></span></td>
<td><span data-ttu-id="d6ac8-305">Octet (8 bits).</span><span class="sxs-lookup"><span data-stu-id="d6ac8-305">A byte (8 bits).</span></span><br/> <span data-ttu-id="d6ac8-306">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-306">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef unsigned char BYTE;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-307"><span id="CALLBACK"></span><span id="callback"></span><strong>RAPPEL</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-307"><span id="CALLBACK"></span><span id="callback"></span><strong>CALLBACK</strong></span></span></td>
<td><span data-ttu-id="d6ac8-308">Convention d’appel pour les fonctions de rappel.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-308">The calling convention for callback functions.</span></span><br/> <span data-ttu-id="d6ac8-309">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-309">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define CALLBACK __stdcall</code><br/> <span data-ttu-id="d6ac8-310">Les fonctions <strong>callback</strong>, <strong>WinAPI</strong>et <strong>APIENTRY</strong> sont toutes utilisées pour définir des fonctions avec la Convention d’appel __stdcall.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-310"><strong>CALLBACK</strong>, <strong>WINAPI</strong>, and <strong>APIENTRY</strong> are all used to define functions with the __stdcall calling convention.</span></span> <span data-ttu-id="d6ac8-311">La plupart des fonctions de l’API Windows sont déclarées à l’aide de <strong>WinAPI</strong>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-311">Most functions in the Windows API are declared using <strong>WINAPI</strong>.</span></span> <span data-ttu-id="d6ac8-312">Vous pouvez utiliser le <strong>rappel</strong> pour les fonctions de rappel que vous implémentez pour aider à identifier la fonction en tant que fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-312">You may wish to use <strong>CALLBACK</strong> for the callback functions that you implement to help identify the function as a callback function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-313"><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-313"><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></span></span></td>
<td><span data-ttu-id="d6ac8-314">Caractère Windows (ANSI) 8 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-314">An 8-bit Windows (ANSI) character.</span></span><br/> <span data-ttu-id="d6ac8-315">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-315">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef char CCHAR;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-316"><span id="CHAR"></span><span id="char"></span><strong>CHAR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-316"><span id="CHAR"></span><span id="char"></span><strong>CHAR</strong></span></span></td>
<td><span data-ttu-id="d6ac8-317">Caractère Windows (ANSI) 8 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-317">An 8-bit Windows (ANSI) character.</span></span> <span data-ttu-id="d6ac8-318">Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-318">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span><br/> <span data-ttu-id="d6ac8-319">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-319">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef char CHAR;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-320"><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-320"><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></span></span></td>
<td><span data-ttu-id="d6ac8-321">Valeur de couleur rouge, vert, bleu (RVB) (32 bits).</span><span class="sxs-lookup"><span data-stu-id="d6ac8-321">The red, green, blue (RGB) color value (32 bits).</span></span> <span data-ttu-id="d6ac8-322">Pour plus d’informations sur ce type, consultez <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d6ac8-322">See <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> for information on this type.</span></span><br/> <span data-ttu-id="d6ac8-323">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-323">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef DWORD COLORREF;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-324"><span id="CONST"></span><span id="const"></span><strong>CONST</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-324"><span id="CONST"></span><span id="const"></span><strong>CONST</strong></span></span></td>
<td><span data-ttu-id="d6ac8-325">Variable dont la valeur doit rester constante pendant l’exécution.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-325">A variable whose value is to remain constant during execution.</span></span> <br/> <span data-ttu-id="d6ac8-326">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-326">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define CONST const</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-327"><span id="DWORD"></span><span id="dword"></span><strong>GRANDE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-327"><span id="DWORD"></span><span id="dword"></span><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="d6ac8-328">Entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-328">A 32-bit unsigned integer.</span></span> <span data-ttu-id="d6ac8-329">La plage est comprise entre 0 et 4294967295 décimale.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-329">The range is 0 through 4294967295 decimal.</span></span><br/> <span data-ttu-id="d6ac8-330">Ce type est déclaré dans IntSafe. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-330">This type is declared in IntSafe.h as follows:</span></span><br/> <code>typedef unsigned long DWORD;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-331"><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-331"><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></span></span></td>
<td><span data-ttu-id="d6ac8-332">Entier 64 bits non signé.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-332">A 64-bit unsigned integer.</span></span> <span data-ttu-id="d6ac8-333">La plage est comprise entre 0 et 18446744073709551615.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-333">The range is 0 through 18446744073709551615 decimal.</span></span><br/> <span data-ttu-id="d6ac8-334">Ce type est déclaré dans IntSafe. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-334">This type is declared in IntSafe.h as follows:</span></span><br/> <code>typedef unsigned __int64 DWORDLONG;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-335"><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-335"><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></span></span></td>
<td><span data-ttu-id="d6ac8-336">Type long non signé pour la précision du pointeur.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-336">An unsigned long type for pointer precision.</span></span> <span data-ttu-id="d6ac8-337">Utilisez lorsque vous effectuez un cast d’un pointeur vers un type long pour effectuer une opération arithmétique de pointeur.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-337">Use when casting a pointer to a long type to perform pointer arithmetic.</span></span> <span data-ttu-id="d6ac8-338">(Également couramment utilisé pour les paramètres 32 bits généraux qui ont été étendus à 64 bits dans Windows 64 bits.)</span><span class="sxs-lookup"><span data-stu-id="d6ac8-338">(Also commonly used for general 32-bit parameters that have been extended to 64 bits in 64-bit Windows.)</span></span><br/> <span data-ttu-id="d6ac8-339">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-339">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef ULONG_PTR DWORD_PTR;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-340"><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-340"><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></span></span></td>
<td><span data-ttu-id="d6ac8-341">Entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-341">A 32-bit unsigned integer.</span></span><br/> <span data-ttu-id="d6ac8-342">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-342">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef unsigned int DWORD32;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-343"><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-343"><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></span></span></td>
<td><span data-ttu-id="d6ac8-344">Entier 64 bits non signé.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-344">A 64-bit unsigned integer.</span></span><br/> <span data-ttu-id="d6ac8-345">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-345">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef unsigned __int64 DWORD64;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-346"><span id="FLOAT"></span><span id="float"></span><strong>DISSOCIÉ</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-346"><span id="FLOAT"></span><span id="float"></span><strong>FLOAT</strong></span></span></td>
<td><span data-ttu-id="d6ac8-347">Variable à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-347">A floating-point variable.</span></span><br/> <span data-ttu-id="d6ac8-348">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-348">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef float FLOAT;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-349"><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-349"><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></span></span></td>
<td><span data-ttu-id="d6ac8-350">Handle d’une <a href="/windows/desktop/menurc/keyboard-accelerators">table d’accélérateurs</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-350">A handle to an <a href="/windows/desktop/menurc/keyboard-accelerators">accelerator table</a>.</span></span><br/> <span data-ttu-id="d6ac8-351">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-351">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef HANDLE HACCEL;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-352"><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-352"><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></span></span></td>
<td><span data-ttu-id="d6ac8-353">La moitié de la taille d’un pointeur.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-353">Half the size of a pointer.</span></span> <span data-ttu-id="d6ac8-354">Utilisez dans une structure qui contient un pointeur et deux petits champs.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-354">Use within a structure that contains a pointer and two small fields.</span></span><br/> <span data-ttu-id="d6ac8-355">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-355">This type is declared in BaseTsd.h as follows:</span></span><br/> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-356">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-356">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef int HALF_PTR;
#else
 typedef short HALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-357"><span id="HANDLE"></span><span id="handle"></span><strong>TRAITÉE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-357"><span id="HANDLE"></span><span id="handle"></span><strong>HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-358">Handle d’un objet.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-358">A handle to an object.</span></span></p>
<p><span data-ttu-id="d6ac8-359">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-359">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef PVOID HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-360"><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-360"><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-361">Handle d’une <a href="/windows/desktop/gdi/bitmaps">bitmap</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-361">A handle to a <a href="/windows/desktop/gdi/bitmaps">bitmap</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-362">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-362">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HBITMAP;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-363"><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-363"><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-364">Handle d’un <a href="/windows/desktop/gdi/brushes">pinceau</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-364">A handle to a <a href="/windows/desktop/gdi/brushes">brush</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-365">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-365">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HBRUSH;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-366"><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-366"><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-367">Handle d’un <a href="/previous-versions//dd316799(v=vs.85)">espace de couleurs</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-367">A handle to a <a href="/previous-versions//dd316799(v=vs.85)">color space</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-368">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-368">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HCOLORSPACE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-369"><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-369"><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-370">Handle d’une conversation DDE (Dynamic Data Exchange).</span><span class="sxs-lookup"><span data-stu-id="d6ac8-370">A handle to a dynamic data exchange (DDE) conversation.</span></span></p>
<p><span data-ttu-id="d6ac8-371">Ce type est déclaré dans Ddeml. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-371">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HCONV;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-372"><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-372"><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-373">Handle d’une liste de conversations DDE.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-373">A handle to a DDE conversation list.</span></span></p>
<p><span data-ttu-id="d6ac8-374">Ce type est déclaré dans Ddeml. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-374">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HCONVLIST;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-375"><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-375"><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-376">Handle d’un <a href="/windows/desktop/menurc/cursors">curseur</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-376">A handle to a <a href="/windows/desktop/menurc/cursors">cursor</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-377">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-377">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HICON HCURSOR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-378"><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-378"><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-379">Handle vers un <a href="/windows/desktop/gdi/device-context-types">contexte de périphérique</a> (DC).</span><span class="sxs-lookup"><span data-stu-id="d6ac8-379">A handle to a <a href="/windows/desktop/gdi/device-context-types">device context</a> (DC).</span></span></p>
<p><span data-ttu-id="d6ac8-380">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-380">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HDC;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-381"><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-381"><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-382">Handle vers les données DDE.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-382">A handle to DDE data.</span></span></p>
<p><span data-ttu-id="d6ac8-383">Ce type est déclaré dans Ddeml. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-383">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HDDEDATA;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-384"><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-384"><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-385">Handle d’un <a href="/windows/desktop/winstation/desktops">Bureau</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-385">A handle to a <a href="/windows/desktop/winstation/desktops">desktop</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-386">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-386">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HDESK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-387"><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-387"><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-388">Handle d’une structure de dépôt interne.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-388">A handle to an internal drop structure.</span></span></p>
<p><span data-ttu-id="d6ac8-389">Ce type est déclaré dans ShellApi. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-389">This type is declared in ShellApi.h as follows:</span></span></p>
<p><code>typedef HANDLE HDROP;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-390"><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-390"><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-391">Handle d’une structure de position de fenêtre différée.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-391">A handle to a deferred window position structure.</span></span></p>
<p><span data-ttu-id="d6ac8-392">Ce type est déclaré dans WinUser. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-392">This type is declared in WinUser.h as follows:</span></span></p>
<p><code>typedef HANDLE HDWP;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-393"><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-393"><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-394">Handle d’un <a href="/windows/desktop/gdi/metafiles">métafichier amélioré</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-394">A handle to an <a href="/windows/desktop/gdi/metafiles">enhanced metafile</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-395">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-395">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HENHMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-396"><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-396"><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-397">Handle vers un fichier ouvert par <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>, et non <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-397">A handle to a file opened by <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>, not <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-398">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-398">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int HFILE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-399"><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-399"><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-400">Handle d’une <a href="/windows/desktop/gdi/about-fonts">police</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-400">A handle to a <a href="/windows/desktop/gdi/about-fonts">font</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-401">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-401">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HFONT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-402"><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>HGDIOBJ</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-402"><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>HGDIOBJ</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-403">Handle d’un objet GDI.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-403">A handle to a GDI object.</span></span></p>
<p><span data-ttu-id="d6ac8-404">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-404">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HGDIOBJ;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-405"><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-405"><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-406">Handle d’un bloc de mémoire globale.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-406">A handle to a global memory block.</span></span></p>
<p><span data-ttu-id="d6ac8-407">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-407">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HGLOBAL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-408"><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-408"><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-409">Handle d’un <a href="/windows/desktop/winmsg/hooks">Hook</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-409">A handle to a <a href="/windows/desktop/winmsg/hooks">hook</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-410">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-410">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HHOOK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-411"><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-411"><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-412">Handle d’une <a href="/windows/desktop/menurc/icons">icône</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-412">A handle to an <a href="/windows/desktop/menurc/icons">icon</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-413">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-413">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HICON;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-414"><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-414"><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-415">Handle d’une instance.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-415">A handle to an instance.</span></span> <span data-ttu-id="d6ac8-416">Il s’agit de l’adresse de base du module en mémoire.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-416">This is the base address of the module in memory.</span></span></p>
<p><span data-ttu-id="d6ac8-417"><strong>HMODULE</strong> et <strong>HINSTANCE</strong> sont les mêmes aujourd’hui, mais représentaient des choses différentes dans Windows 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-417"><strong>HMODULE</strong> and <strong>HINSTANCE</strong> are the same today, but represented different things in 16-bit Windows.</span></span></p>
<p><span data-ttu-id="d6ac8-418">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-418">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HINSTANCE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-419"><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-419"><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-420">Handle d’une clé de registre.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-420">A handle to a registry key.</span></span></p>
<p><span data-ttu-id="d6ac8-421">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-421">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HKEY;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-422"><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-422"><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-423">Identificateur de paramètres régionaux d’entrée.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-423">An input locale identifier.</span></span></p>
<p><span data-ttu-id="d6ac8-424">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-424">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HKL;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-425"><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-425"><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-426">Handle vers un bloc de mémoire local.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-426">A handle to a local memory block.</span></span></p>
<p><span data-ttu-id="d6ac8-427">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-427">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HLOCAL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-428"><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-428"><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-429">Handle d’un <a href="/windows/desktop/menurc/menus">menu</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-429">A handle to a <a href="/windows/desktop/menurc/menus">menu</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-430">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-430">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HMENU;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-431"><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-431"><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-432">Handle d’un <a href="/windows/desktop/gdi/metafiles">métafichier</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-432">A handle to a <a href="/windows/desktop/gdi/metafiles">metafile</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-433">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-433">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-434"><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-434"><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-435">Handle d’un module.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-435">A handle to a module.</span></span> <span data-ttu-id="d6ac8-436">Est l’adresse de base du module en mémoire.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-436">The is the base address of the module in memory.</span></span></p>
<p><span data-ttu-id="d6ac8-437"><strong>HMODULE</strong> et <strong>HINSTANCE</strong> sont les mêmes dans les versions actuelles de Windows, mais représentaient des éléments différents dans Windows 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-437"><strong>HMODULE</strong> and <strong>HINSTANCE</strong> are the same in current versions of Windows, but represented different things in 16-bit Windows.</span></span></p>
<p><span data-ttu-id="d6ac8-438">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-438">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HINSTANCE HMODULE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-439"><span id="HMONITOR"></span><span id="hmonitor"></span><strong>HMONITOR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-439"><span id="HMONITOR"></span><span id="hmonitor"></span><strong>HMONITOR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-440">Handle d’un moniteur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-440">A handle to a display monitor.</span></span></p>
<p><span data-ttu-id="d6ac8-441">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-441">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>if(WINVER >= 0x0500) typedef HANDLE HMONITOR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-442"><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-442"><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-443">Handle d’une palette.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-443">A handle to a palette.</span></span></p>
<p><span data-ttu-id="d6ac8-444">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-444">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HPALETTE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-445"><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-445"><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-446">Handle d’un <a href="/windows/desktop/gdi/pens">stylet</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-446">A handle to a <a href="/windows/desktop/gdi/pens">pen</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-447">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-447">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HPEN;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-448"><span id="HRESULT"></span><span id="hresult"></span><strong>SIGNÉ</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-448"><span id="HRESULT"></span><span id="hresult"></span><strong>HRESULT</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-449">Codes de retour utilisés par les interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-449">The return codes used by COM interfaces.</span></span> <span data-ttu-id="d6ac8-450">Pour plus d’informations, consultez <a href="/windows/desktop/com/structure-of-com-error-codes">structure des codes d’erreur com</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-450">For more information, see <a href="/windows/desktop/com/structure-of-com-error-codes">Structure of the COM Error Codes</a>.</span></span> <span data-ttu-id="d6ac8-451">Pour tester une valeur <strong>HRESULT</strong> , utilisez les macros <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>failed</strong></a> et <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>Succeeded</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d6ac8-451">To test an <strong>HRESULT</strong> value, use the <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>FAILED</strong></a> and <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>SUCCEEDED</strong></a> macros.</span></span></p>
<p><span data-ttu-id="d6ac8-452">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-452">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONG HRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-453"><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-453"><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-454">Handle vers une <a href="/windows/desktop/gdi/regions">région</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-454">A handle to a <a href="/windows/desktop/gdi/regions">region</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-455">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-455">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HRGN;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-456"><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-456"><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-457">Handle d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-457">A handle to a resource.</span></span></p>
<p><span data-ttu-id="d6ac8-458">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-458">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HRSRC;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-459"><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-459"><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-460">Handle d’une chaîne DDE.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-460">A handle to a DDE string.</span></span></p>
<p><span data-ttu-id="d6ac8-461">Ce type est déclaré dans Ddeml. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-461">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HSZ;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-462"><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-462"><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-463">Handle d’une <a href="/windows/desktop/winstation/window-stations">station Windows</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-463">A handle to a <a href="/windows/desktop/winstation/window-stations">window station</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-464">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-464">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE WINSTA;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-465"><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-465"><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-466">Handle d’une <a href="/windows/desktop/winmsg/windows">fenêtre</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-466">A handle to a <a href="/windows/desktop/winmsg/windows">window</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-467">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-467">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HWND;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-468"><span id="INT"></span><span id="int"></span><strong>TIERS</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-468"><span id="INT"></span><span id="int"></span><strong>INT</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-469">Entier signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-469">A 32-bit signed integer.</span></span> <span data-ttu-id="d6ac8-470">La plage est comprise entre-2147483648 et 2147483647 décimal.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-470">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="d6ac8-471">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-471">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int INT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-472"><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-472"><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-473">Type entier signé pour la précision du pointeur.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-473">A signed integer type for pointer precision.</span></span> <span data-ttu-id="d6ac8-474">Utilisez lorsque vous effectuez un cast d’un pointeur vers un entier pour effectuer une opération arithmétique de pointeur.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-474">Use when casting a pointer to an integer to perform pointer arithmetic.</span></span></p>
<p><span data-ttu-id="d6ac8-475">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-475">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-476">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-476">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64) 
 typedef __int64 INT_PTR; 
#else 
 typedef int INT_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-477"><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-477"><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-478">Entier signé 8 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-478">An 8-bit signed integer.</span></span></p>
<p><span data-ttu-id="d6ac8-479">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-479">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed char INT8;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-480"><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-480"><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-481">Entier signé 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-481">A 16-bit signed integer.</span></span></p>
<p><span data-ttu-id="d6ac8-482">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-482">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed short INT16;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-483"><span id="INT32"></span><span id="int32"></span><strong>ENTIER</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-483"><span id="INT32"></span><span id="int32"></span><strong>INT32</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-484">Entier signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-484">A 32-bit signed integer.</span></span> <span data-ttu-id="d6ac8-485">La plage est comprise entre-2147483648 et 2147483647 décimal.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-485">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="d6ac8-486">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-486">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed int INT32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-487"><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-487"><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-488">Entier signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-488">A 64-bit signed integer.</span></span> <span data-ttu-id="d6ac8-489">La plage est comprise entre-9223372036854775808 et 9223372036854775807 décimale.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-489">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="d6ac8-490">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-490">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed __int64 INT64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-491"><span id="LANGID"></span><span id="langid"></span><strong>LANGID</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-491"><span id="LANGID"></span><span id="langid"></span><strong>LANGID</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-492">Identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-492">A language identifier.</span></span> <span data-ttu-id="d6ac8-493">Pour plus d’informations, consultez <a href="/windows/desktop/Intl/language-identifiers">identificateurs de langue</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-493">For more information, see <a href="/windows/desktop/Intl/language-identifiers">Language Identifiers</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-494">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-494">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WORD LANGID;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-495"><span id="LCID"></span><span id="lcid"></span><strong>LCID</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-495"><span id="LCID"></span><span id="lcid"></span><strong>LCID</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-496">Identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-496">A locale identifier.</span></span> <span data-ttu-id="d6ac8-497">Pour plus d’informations, consultez <a href="/windows/desktop/Intl/locale-identifiers">identificateurs de paramètres régionaux</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-497">For more information, see <a href="/windows/desktop/Intl/locale-identifiers">Locale Identifiers</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-498">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-498">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef DWORD LCID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-499"><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-499"><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-500">Type d’informations de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-500">A locale information type.</span></span> <span data-ttu-id="d6ac8-501">Pour obtenir une liste, consultez <a href="/windows/desktop/Intl/locale-information-constants">constantes d’informations relatives aux paramètres régionaux</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-501">For a list, see <a href="/windows/desktop/Intl/locale-information-constants">Locale Information Constants</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-502">Ce type est déclaré dans WinNls. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-502">This type is declared in WinNls.h as follows:</span></span></p>
<p><code>typedef DWORD LCTYPE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-503"><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-503"><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-504">Identificateur du groupe de langues.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-504">A language group identifier.</span></span> <span data-ttu-id="d6ac8-505">Pour obtenir une liste, consultez <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-505">For a list, see <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-506">Ce type est déclaré dans WinNls. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-506">This type is declared in WinNls.h as follows:</span></span></p>
<p><code>typedef DWORD LGRPID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-507"><span id="LONG"></span><span id="long"></span><strong>LONG</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-507"><span id="LONG"></span><span id="long"></span><strong>LONG</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-508">Entier signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-508">A 32-bit signed integer.</span></span> <span data-ttu-id="d6ac8-509">La plage est comprise entre-2147483648 et 2147483647 décimal.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-509">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="d6ac8-510">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-510">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef long LONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-511"><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-511"><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-512">Entier signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-512">A 64-bit signed integer.</span></span> <span data-ttu-id="d6ac8-513">La plage est comprise entre-9223372036854775808 et 9223372036854775807 décimale.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-513">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="d6ac8-514">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-514">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-515">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-515">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if !defined(_M_IX86)
 typedef __int64 LONGLONG; 
#else
 typedef double LONGLONG;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-516"><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-516"><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-517">Type long signé pour la précision du pointeur.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-517">A signed long type for pointer precision.</span></span> <span data-ttu-id="d6ac8-518">Utilisez lorsque vous effectuez un cast d’un pointeur vers un long pour effectuer une opération arithmétique de pointeur.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-518">Use when casting a pointer to a long to perform pointer arithmetic.</span></span></p>
<p><span data-ttu-id="d6ac8-519">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-519">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-520">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-520">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef __int64 LONG_PTR; 
#else
 typedef long LONG_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-521"><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-521"><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-522">Entier signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-522">A 32-bit signed integer.</span></span> <span data-ttu-id="d6ac8-523">La plage est comprise entre-2147483648 et 2147483647 décimal.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-523">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="d6ac8-524">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-524">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed int LONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-525"><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-525"><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-526">Entier signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-526">A 64-bit signed integer.</span></span> <span data-ttu-id="d6ac8-527">La plage est comprise entre-9223372036854775808 et 9223372036854775807 décimale.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-527">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="d6ac8-528">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-528">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef __int64 LONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-529"><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-529"><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-530">Paramètre de message.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-530">A message parameter.</span></span></p>
<p><span data-ttu-id="d6ac8-531">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-531">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef LONG_PTR LPARAM;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-532"><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-532"><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-533">Pointeur vers un <a href="#bool"><strong>booléen</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-533">A pointer to a <a href="#bool"><strong>BOOL</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-534">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-534">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BOOL far *LPBOOL;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-535"><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-535"><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-536">Pointeur vers un <a href="#byte"><strong>octet</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-536">A pointer to a <a href="#byte"><strong>BYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-537">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-537">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BYTE far *LPBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-538"><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-538"><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-539">Pointeur vers une valeur <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d6ac8-539">A pointer to a <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> value.</span></span></p>
<p><span data-ttu-id="d6ac8-540">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-540">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *LPCOLORREF;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-541"><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-541"><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-542">Pointeur vers une chaîne constante se terminant par un caractère null de caractères Windows (ANSI) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-542">A pointer to a constant null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="d6ac8-543">Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-543">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-544">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-544">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef __nullterminated CONST CHAR *LPCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-545"><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-545"><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-546">Un <a href="#lpcwstr"><strong>LPCWSTR</strong></a> si <strong>Unicode</strong> est défini, un <a href="#lpcstr"><strong>LPCSTR</strong></a> dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-546">An <a href="#lpcwstr"><strong>LPCWSTR</strong></a> if <strong>UNICODE</strong> is defined, an <a href="#lpcstr"><strong>LPCSTR</strong></a> otherwise.</span></span> <span data-ttu-id="d6ac8-547">Pour plus d’informations, consultez <a href="/windows/desktop/Intl/windows-data-types-for-strings">types de données Windows pour les chaînes</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-547">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-548">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-548">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-549">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-549">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPCWSTR LPCTSTR; 
#else
 typedef LPCSTR LPCTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-550"><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-550"><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-551">Pointeur vers une constante de tout type.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-551">A pointer to a constant of any type.</span></span></p>
<p><span data-ttu-id="d6ac8-552">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-552">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef CONST void *LPCVOID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-553"><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-553"><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-554">Pointeur vers une chaîne constante se terminant par null de caractères Unicode 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-554">A pointer to a constant null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="d6ac8-555">Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-555">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-556">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-556">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST WCHAR *LPCWSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-557"><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-557"><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-558">Pointeur vers une <a href="#dword"><strong>valeur DWORD</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-558">A pointer to a <a href="#dword"><strong>DWORD</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-559">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-559">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *LPDWORD;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-560"><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-560"><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-561">Pointeur vers un <a href="#handle"><strong>handle</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-561">A pointer to a <a href="#handle"><strong>HANDLE</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-562">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-562">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE *LPHANDLE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-563"><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-563"><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-564">Pointeur vers un <a href="#int"><strong>entier</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-564">A pointer to an <a href="#int"><strong>INT</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-565">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-565">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int *LPINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-566"><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-566"><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-567">Pointeur vers une <a href="#long"><strong>valeur long</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-567">A pointer to a <a href="#long"><strong>LONG</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-568">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-568">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef long *LPLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-569"><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-569"><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-570">Pointeur vers une chaîne se terminant par un caractère null de caractères Windows (ANSI) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-570">A pointer to a null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="d6ac8-571">Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-571">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-572">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-572">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *LPSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-573"><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-573"><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-574">Un <a href="#lpwstr"><strong>LPWStr</strong></a> si <strong>Unicode</strong> est défini, sinon, <a href="#lpstr"><strong>LPSTR</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d6ac8-574">An <a href="#lpwstr"><strong>LPWSTR</strong></a> if <strong>UNICODE</strong> is defined, an <a href="#lpstr"><strong>LPSTR</strong></a> otherwise.</span></span> <span data-ttu-id="d6ac8-575">Pour plus d’informations, consultez <a href="/windows/desktop/Intl/windows-data-types-for-strings">types de données Windows pour les chaînes</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-575">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-576">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-576">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-577">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-577">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPWSTR LPTSTR;
#else
 typedef LPSTR LPTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-578"><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-578"><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-579">Pointeur vers n’importe quel type.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-579">A pointer to any type.</span></span></p>
<p><span data-ttu-id="d6ac8-580">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-580">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef void *LPVOID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-581"><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-581"><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-582">Pointeur vers un <a href="#word"><strong>mot</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-582">A pointer to a <a href="#word"><strong>WORD</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-583">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-583">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef WORD *LPWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-584"><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-584"><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-585">Pointeur vers une chaîne se terminant par un caractère null de caractères Unicode 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-585">A pointer to a null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="d6ac8-586">Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-586">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-587">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-587">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *LPWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-588"><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-588"><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-589">Résultat signé du traitement du message.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-589">Signed result of message processing.</span></span></p>
<p><span data-ttu-id="d6ac8-590">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-590">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef LONG_PTR LRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-591"><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-591"><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-592">Pointeur vers un <a href="#bool"><strong>booléen</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-592">A pointer to a <a href="#bool"><strong>BOOL</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-593">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-593">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BOOL *PBOOL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-594"><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-594"><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-595">Pointeur vers une <a href="#boolean"><strong>valeur booléenne</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-595">A pointer to a <a href="#boolean"><strong>BOOLEAN</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-596">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-596">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef BOOLEAN *PBOOLEAN;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-597"><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-597"><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-598">Pointeur vers un <a href="#byte"><strong>octet</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-598">A pointer to a <a href="#byte"><strong>BYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-599">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-599">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BYTE *PBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-600"><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-600"><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-601">Pointeur vers un <a href="#char"><strong>caractère</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-601">A pointer to a <a href="#char"><strong>CHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-602">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-602">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *PCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-603"><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-603"><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-604">Pointeur vers une chaîne constante se terminant par un caractère null de caractères Windows (ANSI) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-604">A pointer to a constant null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="d6ac8-605">Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-605">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-606">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-606">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST CHAR *PCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-607"><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-607"><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-608">Un <a href="#pcwstr"><strong>PCWSTR</strong></a> si <strong>Unicode</strong> est défini, un <a href="#pcstr"><strong>PCSTR</strong></a> dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-608">A <a href="#pcwstr"><strong>PCWSTR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#pcstr"><strong>PCSTR</strong></a> otherwise.</span></span> <span data-ttu-id="d6ac8-609">Pour plus d’informations, consultez <a href="/windows/desktop/Intl/windows-data-types-for-strings">types de données Windows pour les chaînes</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-609">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-610">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-610">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-611">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-611">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPCWSTR PCTSTR;
#else
 typedef LPCSTR PCTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-612"><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-612"><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-613">Pointeur vers une chaîne constante se terminant par null de caractères Unicode 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-613">A pointer to a constant null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="d6ac8-614">Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-614">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-615">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-615">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST WCHAR *PCWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-616"><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-616"><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-617">Pointeur vers une <a href="#dword"><strong>valeur DWORD</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-617">A pointer to a <a href="#dword"><strong>DWORD</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-618">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-618">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *PDWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-619"><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-619"><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-620">Pointeur vers un <a href="#dwordlong"><strong>DWORDLONG</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-620">A pointer to a <a href="#dwordlong"><strong>DWORDLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-621">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-621">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef DWORDLONG *PDWORDLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-622"><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-622"><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-623">Pointeur vers un <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-623">A pointer to a <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-624">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-624">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD_PTR *PDWORD_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-625"><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-625"><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-626">Pointeur vers un <a href="#dword32"><strong>DWORD32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-626">A pointer to a <a href="#dword32"><strong>DWORD32</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-627">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-627">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD32 *PDWORD32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-628"><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-628"><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-629">Pointeur vers un <a href="#dword64"><strong>DWORD64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-629">A pointer to a <a href="#dword64"><strong>DWORD64</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-630">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-630">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD64 *PDWORD64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-631"><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-631"><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-632">Pointeur vers un <a href="#float"><strong>float</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-632">A pointer to a <a href="#float"><strong>FLOAT</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-633">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-633">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef FLOAT *PFLOAT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-634"><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-634"><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-635">Pointeur vers un <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-635">A pointer to a <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-636">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-636">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-637">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-637">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef HALF_PTR *PHALF_PTR;
#else
 typedef HALF_PTR *PHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-638"><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-638"><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-639">Pointeur vers un <a href="#handle"><strong>handle</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-639">A pointer to a <a href="#handle"><strong>HANDLE</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-640">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-640">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef HANDLE *PHANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-641"><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-641"><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-642">Pointeur vers un <a href="#hkey"><strong>HKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-642">A pointer to an <a href="#hkey"><strong>HKEY</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-643">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-643">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HKEY *PHKEY;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-644"><span id="PINT"></span><span id="pint"></span><strong>VIENNENT</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-644"><span id="PINT"></span><span id="pint"></span><strong>PINT</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-645">Pointeur vers un <a href="#int"><strong>entier</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-645">A pointer to an <a href="#int"><strong>INT</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-646">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-646">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int *PINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-647"><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-647"><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-648">Pointeur vers un <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-648">A pointer to an <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-649">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-649">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT_PTR *PINT_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-650"><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-650"><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-651">Pointeur vers <a href="#int8"><strong>INT8</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-651">A pointer to an <a href="#int8"><strong>INT8</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-652">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-652">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT8 *PINT8;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-653"><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-653"><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-654">Pointeur vers un <a href="#int16"><strong>Int16</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-654">A pointer to an <a href="#int16"><strong>INT16</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-655">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-655">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT16 *PINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-656"><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-656"><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-657">Pointeur vers un <a href="#int32"><strong>Int32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-657">A pointer to an <a href="#int32"><strong>INT32</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-658">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-658">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT32 *PINT32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-659"><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-659"><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-660">Pointeur vers un <a href="#int64"><strong>Int64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-660">A pointer to an <a href="#int64"><strong>INT64</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-661">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-661">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT64 *PINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-662"><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-662"><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-663">Pointeur vers un <a href="#lcid"><strong>LCID</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-663">A pointer to an <a href="#lcid"><strong>LCID</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-664">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-664">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef PDWORD PLCID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-665"><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-665"><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-666">Pointeur vers une <a href="#long"><strong>valeur long</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-666">A pointer to a <a href="#long"><strong>LONG</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-667">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-667">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONG *PLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-668"><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-668"><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-669">Pointeur vers un <a href="#longlong"><strong>LongLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-669">A pointer to a <a href="#longlong"><strong>LONGLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-670">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-670">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONGLONG *PLONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-671"><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-671"><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-672">Pointeur vers un <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-672">A pointer to a <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-673">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-673">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG_PTR *PLONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-674"><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-674"><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-675">Pointeur vers un <a href="#long32"><strong>LONG32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-675">A pointer to a <a href="#long32"><strong>LONG32</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-676">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-676">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG32 *PLONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-677"><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-677"><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-678">Pointeur vers un <a href="#long64"><strong>LONG64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-678">A pointer to a <a href="#long64"><strong>LONG64</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-679">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-679">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG64 *PLONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-680"><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-680"><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-681">Pointeur 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-681">A 32-bit pointer.</span></span> <span data-ttu-id="d6ac8-682">Sur un système 32 bits, il s’agit d’un pointeur natif.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-682">On a 32-bit system, this is a native pointer.</span></span> <span data-ttu-id="d6ac8-683">Sur un système 64 bits, il s’agit d’un pointeur 64 bits tronqué.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-683">On a 64-bit system, this is a truncated 64-bit pointer.</span></span></p>
<p><span data-ttu-id="d6ac8-684">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-684">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-685">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-685">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
#define POINTER_32 __ptr32
#else
#define POINTER_32
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-686"><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-686"><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-687">Pointeur 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-687">A 64-bit pointer.</span></span> <span data-ttu-id="d6ac8-688">Sur un système 64 bits, il s’agit d’un pointeur natif.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-688">On a 64-bit system, this is a native pointer.</span></span> <span data-ttu-id="d6ac8-689">Sur un système 32 bits, il s’agit d’un pointeur 32 bits étendu au niveau du signe.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-689">On a 32-bit system, this is a sign-extended 32-bit pointer.</span></span></p>
<p><span data-ttu-id="d6ac8-690">Notez qu’il n’est pas possible de supposer l’état du bit de pointeur le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-690">Note that it is not safe to assume the state of the high pointer bit.</span></span></p>
<p><span data-ttu-id="d6ac8-691">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-691">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-692">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-692">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if (_MSC_VER >= 1300)
#define POINTER_64 __ptr64
#else
#define POINTER_64
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-693"><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-693"><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-694">Pointeur signé.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-694">A signed pointer.</span></span></p>
<p><span data-ttu-id="d6ac8-695">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-695">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>#define POINTER_SIGNED __sptr</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-696"><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-696"><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-697">Pointeur non signé.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-697">An unsigned pointer.</span></span></p>
<p><span data-ttu-id="d6ac8-698">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-698">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>#define POINTER_UNSIGNED __uptr</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-699"><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-699"><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-700">Pointeur vers un <a href="#short"><strong>short</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-700">A pointer to a <a href="#short"><strong>SHORT</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-701">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-701">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef SHORT *PSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-702"><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-702"><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-703">Pointeur vers un <a href="#size_t"><strong>size_t</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-703">A pointer to a <a href="#size_t"><strong>SIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-704">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-704">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef SIZE_T *PSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-705"><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-705"><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-706">Pointeur vers un <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-706">A pointer to a <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-707">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-707">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef SSIZE_T *PSSIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-708"><span id="PSTR"></span><span id="pstr"></span><strong>PSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-708"><span id="PSTR"></span><span id="pstr"></span><strong>PSTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-709">Pointeur vers une chaîne se terminant par un caractère null de caractères Windows (ANSI) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-709">A pointer to a null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="d6ac8-710">Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-710">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-711">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-711">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *PSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-712"><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-712"><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-713">Pointeur vers un <a href="#tbyte"><strong>to</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-713">A pointer to a <a href="#tbyte"><strong>TBYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-714">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-714">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef TBYTE *PTBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-715"><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-715"><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-716">Pointeur vers un <a href="#tchar"><strong>TCHAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-716">A pointer to a <a href="#tchar"><strong>TCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-717">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-717">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef TCHAR *PTCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-718"><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-718"><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-719">Un <a href="#pwstr"><strong>PWSTR</strong></a> si <strong>Unicode</strong> est défini, un <a href="#pstr"><strong>PSTR</strong></a> dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-719">A <a href="#pwstr"><strong>PWSTR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#pstr"><strong>PSTR</strong></a> otherwise.</span></span> <span data-ttu-id="d6ac8-720">Pour plus d’informations, consultez <a href="/windows/desktop/Intl/windows-data-types-for-strings">types de données Windows pour les chaînes</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-720">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-721">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-721">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-722">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-722">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPWSTR PTSTR;
#else typedef LPSTR PTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-723"><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-723"><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-724">Pointeur vers un <a href="#uchar"><strong>UCHAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-724">A pointer to a <a href="#uchar"><strong>UCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-725">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-725">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UCHAR *PUCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-726"><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-726"><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-727">Pointeur vers un <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-727">A pointer to a <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-728">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-728">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-729">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-729">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef UHALF_PTR *PUHALF_PTR;
#else
 typedef UHALF_PTR *PUHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-730"><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-730"><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-731">Pointeur vers un <a href="#uint"><strong>uint</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-731">A pointer to a <a href="#uint"><strong>UINT</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-732">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-732">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UINT *PUINT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-733"><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-733"><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-734">Pointeur vers un <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-734">A pointer to a <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-735">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-735">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT_PTR *PUINT_PTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-736"><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-736"><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-737">Pointeur vers <a href="#uint8"><strong>UINT8</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-737">A pointer to a <a href="#uint8"><strong>UINT8</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-738">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-738">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT8 *PUINT8;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-739"><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-739"><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-740">Pointeur vers <a href="#uint16"><strong>UINT16</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-740">A pointer to a <a href="#uint16"><strong>UINT16</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-741">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-741">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT16 *PUINT16;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-742"><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-742"><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-743">Pointeur vers un <a href="#uint32"><strong>UInt32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-743">A pointer to a <a href="#uint32"><strong>UINT32</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-744">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-744">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT32 *PUINT32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-745"><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-745"><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-746">Pointeur vers un <a href="#uint64"><strong>UINT64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-746">A pointer to a <a href="#uint64"><strong>UINT64</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-747">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-747">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT64 *PUINT64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-748"><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-748"><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-749">Pointeur vers un <a href="#ulong"><strong>ULong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-749">A pointer to a <a href="#ulong"><strong>ULONG</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-750">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-750">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef ULONG *PULONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-751"><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-751"><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-752">Pointeur vers un <a href="#ulonglong"><strong>ULONGLONG</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-752">A pointer to a <a href="#ulonglong"><strong>ULONGLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-753">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-753">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef ULONGLONG *PULONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-754"><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-754"><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-755">Pointeur vers un <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-755">A pointer to a <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-756">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-756">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG_PTR *PULONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-757"><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-757"><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-758">Pointeur vers un <a href="#ulong32"><strong>ULONG32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-758">A pointer to a <a href="#ulong32"><strong>ULONG32</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-759">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-759">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG32 *PULONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-760"><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-760"><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-761">Pointeur vers un <a href="#ulong64"><strong>ULONG64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-761">A pointer to a <a href="#ulong64"><strong>ULONG64</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-762">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-762">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG64 *PULONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-763"><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-763"><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-764">Pointeur vers un <a href="#ushort"><strong>UShort</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-764">A pointer to a <a href="#ushort"><strong>USHORT</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-765">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-765">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef USHORT *PUSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-766"><span id="PVOID"></span><span id="pvoid"></span><strong>DÉSIGNE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-766"><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-767">Pointeur vers n’importe quel type.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-767">A pointer to any type.</span></span></p>
<p><span data-ttu-id="d6ac8-768">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-768">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef void *PVOID;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-769"><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-769"><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-770">Pointeur vers un <a href="#wchar"><strong>WCHAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-770">A pointer to a <a href="#wchar"><strong>WCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-771">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-771">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *PWCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-772"><span id="PWORD"></span><span id="pword"></span><strong>PWORD</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-772"><span id="PWORD"></span><span id="pword"></span><strong>PWORD</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-773">Pointeur vers un <a href="#word"><strong>mot</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-773">A pointer to a <a href="#word"><strong>WORD</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-774">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-774">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef WORD *PWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-775"><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-775"><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-776">Pointeur vers une chaîne se terminant par un caractère null de caractères Unicode 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-776">A pointer to a null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="d6ac8-777">Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-777">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-778">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-778">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *PWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-779"><span id="QWORD"></span><span id="qword"></span><strong>Q</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-779"><span id="QWORD"></span><span id="qword"></span><strong>QWORD</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-780">Entier 64 bits non signé.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-780">A 64-bit unsigned integer.</span></span></p>
<p><span data-ttu-id="d6ac8-781">Ce type est déclaré comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-781">This type is declared as follows:</span></span></p>
<p><code>typedef unsigned __int64 QWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-782"><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-782"><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-783">Handle d’une base de données du gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-783">A handle to a service control manager database.</span></span> <span data-ttu-id="d6ac8-784">Pour plus d’informations, consultez <a href="/windows/desktop/Services/scm-handles">Handles SCM</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-784">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-785">Ce type est déclaré dans WinSvc. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-785">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef HANDLE SC_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-786"><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-786"><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-787">Verrou vers une base de données du gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-787">A lock to a service control manager database.</span></span> <span data-ttu-id="d6ac8-788">Pour plus d’informations, consultez <a href="/windows/desktop/Services/scm-handles">Handles SCM</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-788">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-789">Ce type est déclaré dans WinSvc. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-789">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef LPVOID SC_LOCK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-790"><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-790"><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-791">Handle d’une valeur d’état de service.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-791">A handle to a service status value.</span></span> <span data-ttu-id="d6ac8-792">Pour plus d’informations, consultez <a href="/windows/desktop/Services/scm-handles">Handles SCM</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-792">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-793">Ce type est déclaré dans WinSvc. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-793">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef HANDLE SERVICE_STATUS_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-794"><span id="SHORT"></span><span id="short"></span><strong>Résumé</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-794"><span id="SHORT"></span><span id="short"></span><strong>SHORT</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-795">Entier 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-795">A 16-bit integer.</span></span> <span data-ttu-id="d6ac8-796">La plage est comprise entre-32768 et 32767 décimal.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-796">The range is -32768 through 32767 decimal.</span></span></p>
<p><span data-ttu-id="d6ac8-797">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-797">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef short SHORT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-798"><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-798"><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-799">Nombre maximal d’octets auxquels un pointeur peut pointer.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-799">The maximum number of bytes to which a pointer can point.</span></span> <span data-ttu-id="d6ac8-800">Utilisez pour un nombre qui doit s’étendre à la plage complète d’un pointeur.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-800">Use for a count that must span the full range of a pointer.</span></span></p>
<p><span data-ttu-id="d6ac8-801">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-801">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG_PTR SIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-802"><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-802"><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-803">Version signée de <a href="#size_t"><strong>size_t</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-803">A signed version of <a href="#size_t"><strong>SIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-804">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-804">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG_PTR SSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-805"><span id="TBYTE"></span><span id="tbyte"></span><strong>OCTET</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-805"><span id="TBYTE"></span><span id="tbyte"></span><strong>TBYTE</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-806"><a href="#wchar"><strong>WCHAR</strong></a> si <strong>Unicode</strong> est défini, sinon, un <a href="#char"><strong>caractère</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d6ac8-806">A <a href="#wchar"><strong>WCHAR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#char"><strong>CHAR</strong></a> otherwise.</span></span></p>
<p><span data-ttu-id="d6ac8-807">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-807">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-808">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-808">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef WCHAR TBYTE;
#else
 typedef unsigned char TBYTE;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-809"><span id="TCHAR"></span><span id="tchar"></span><strong>TCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-809"><span id="TCHAR"></span><span id="tchar"></span><strong>TCHAR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-810"><a href="#wchar"><strong>WCHAR</strong></a> si <strong>Unicode</strong> est défini, sinon, un <a href="#char"><strong>caractère</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d6ac8-810">A <a href="#wchar"><strong>WCHAR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#char"><strong>CHAR</strong></a> otherwise.</span></span></p>
<p><span data-ttu-id="d6ac8-811">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-811">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-812">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-812">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef WCHAR TCHAR;
#else
 typedef char TCHAR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-813"><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-813"><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-814"><a href="#char"><strong>Caractère</strong></a>non signé.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-814">An unsigned <a href="#char"><strong>CHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-815">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-815">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned char UCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-816"><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-816"><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-817"><a href="#half_ptr"><strong>HALF_PTR</strong></a>non signé.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-817">An unsigned <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span></span> <span data-ttu-id="d6ac8-818">Utilisez dans une structure qui contient un pointeur et deux petits champs.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-818">Use within a structure that contains a pointer and two small fields.</span></span></p>
<p><span data-ttu-id="d6ac8-819">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-819">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-820">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-820">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef unsigned int UHALF_PTR;
#else
 typedef unsigned short UHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-821"><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-821"><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-822"><a href="#int"><strong>Entier</strong></a>non signé.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-822">An unsigned <a href="#int"><strong>INT</strong></a>.</span></span> <span data-ttu-id="d6ac8-823">La plage est comprise entre 0 et 4294967295 décimale.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-823">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="d6ac8-824">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-824">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned int UINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-825"><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-825"><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-826"><a href="#int_ptr"><strong>INT_PTR</strong></a>non signé.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-826">An unsigned <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-827">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-827">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-828">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-828">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef unsigned __int64 UINT_PTR;
#else
 typedef unsigned int UINT_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-829"><span id="UINT8"></span><span id="uint8"></span><strong>DESTINÉES</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-829"><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-830">Unsigned <a href="#int8"><strong>INT8</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-830">An unsigned <a href="#int8"><strong>INT8</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-831">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-831">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned  char UINT8;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-832"><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-832"><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-833">Unsigned <a href="#int16"><strong>Int16</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-833">An unsigned <a href="#int16"><strong>INT16</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-834">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-834">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned  short UINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-835"><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-835"><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-836">Unsigned <a href="#int32"><strong>Int32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-836">An unsigned <a href="#int32"><strong>INT32</strong></a>.</span></span> <span data-ttu-id="d6ac8-837">La plage est comprise entre 0 et 4294967295 décimale.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-837">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="d6ac8-838">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-838">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned int UINT32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-839"><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-839"><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-840">Unsigned <a href="#int64"><strong>Int64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-840">An unsigned <a href="#int64"><strong>INT64</strong></a>.</span></span> <span data-ttu-id="d6ac8-841">La plage est comprise entre 0 et 18446744073709551615.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-841">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="d6ac8-842">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-842">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef usigned __int 64 UINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-843"><span id="ULONG"></span><span id="ulong"></span><strong>CORRESPONDANTE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-843"><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-844"><a href="#long"><strong>Long</strong></a>non signé.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-844">An unsigned <a href="#long"><strong>LONG</strong></a>.</span></span> <span data-ttu-id="d6ac8-845">La plage est comprise entre 0 et 4294967295 décimale.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-845">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="d6ac8-846">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-846">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned long ULONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-847"><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-847"><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-848">Entier 64 bits non signé.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-848">A 64-bit unsigned integer.</span></span> <span data-ttu-id="d6ac8-849">La plage est comprise entre 0 et 18446744073709551615.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-849">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="d6ac8-850">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-850">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-851">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-851">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if !defined(_M_IX86)
 typedef unsigned __int64 ULONGLONG;
#else
 typedef double ULONGLONG;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-852"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-852"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-853"><a href="#long_ptr"><strong>LONG_PTR</strong></a>non signé.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-853">An unsigned <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="d6ac8-854">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-854">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-855">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-855">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef unsigned __int64 ULONG_PTR;
#else
 typedef unsigned long ULONG_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-856"><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-856"><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-857"><a href="#long32"><strong>LONG32</strong></a>non signé.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-857">An unsigned <a href="#long32"><strong>LONG32</strong></a>.</span></span> <span data-ttu-id="d6ac8-858">La plage est comprise entre 0 et 4294967295 décimale.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-858">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="d6ac8-859">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-859">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned int ULONG32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-860"><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-860"><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-861"><a href="#long64"><strong>LONG64</strong></a>non signé.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-861">An unsigned <a href="#long64"><strong>LONG64</strong></a>.</span></span> <span data-ttu-id="d6ac8-862">La plage est comprise entre 0 et 18446744073709551615.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-862">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="d6ac8-863">Ce type est déclaré dans BaseTsd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-863">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned __int64 ULONG64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-864"><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-864"><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-865">Chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-865">A Unicode string.</span></span></p>
<p><span data-ttu-id="d6ac8-866">Ce type est déclaré dans winternl. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-866">This type is declared in Winternl.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6ac8-867">C++</span><span class="sxs-lookup"><span data-stu-id="d6ac8-867">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>typedef struct _UNICODE_STRING {
  USHORT  Length;
  USHORT  MaximumLength;
  PWSTR  Buffer;
} UNICODE_STRING;
typedef UNICODE_STRING *PUNICODE_STRING;
typedef const UNICODE_STRING *PCUNICODE_STRING;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-868"><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-868"><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-869">Unsigned <a href="#short"><strong>short</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-869">An unsigned <a href="#short"><strong>SHORT</strong></a>.</span></span> <span data-ttu-id="d6ac8-870">La plage est comprise entre 0 et 65535 décimale.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-870">The range is 0 through 65535 decimal.</span></span></p>
<p><span data-ttu-id="d6ac8-871">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-871">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned short USHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-872"><span id="USN"></span><span id="usn"></span><strong>NNUMÉRO</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-872"><span id="USN"></span><span id="usn"></span><strong>USN</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-873">Numéro de séquence de mise à jour (USN).</span><span class="sxs-lookup"><span data-stu-id="d6ac8-873">An update sequence number (USN).</span></span></p>
<p><span data-ttu-id="d6ac8-874">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-874">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONGLONG USN;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-875"><span id="VOID"></span><span id="void"></span><strong>NULLITÉ</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-875"><span id="VOID"></span><span id="void"></span><strong>VOID</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-876">Tout type.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-876">Any type.</span></span></p>
<p><span data-ttu-id="d6ac8-877">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-877">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>#define VOID void</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-878"><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-878"><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-879">Caractère Unicode 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-879">A 16-bit Unicode character.</span></span> <span data-ttu-id="d6ac8-880">Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-880">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="d6ac8-881">Ce type est déclaré dans Winnt. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-881">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef wchar_t WCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-882"><span id="WINAPI"></span><span id="winapi"></span><strong>WINAPI</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-882"><span id="WINAPI"></span><span id="winapi"></span><strong>WINAPI</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-883">Convention d’appel pour les fonctions système.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-883">The calling convention for system functions.</span></span></p>
<p><span data-ttu-id="d6ac8-884">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-884">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>#define WINAPI __stdcall</code></p>
<p><span data-ttu-id="d6ac8-885">Les fonctions <strong>callback</strong>, <strong>WinAPI</strong>et <strong>APIENTRY</strong> sont toutes utilisées pour définir des fonctions avec la Convention d’appel __stdcall.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-885"><strong>CALLBACK</strong>, <strong>WINAPI</strong>, and <strong>APIENTRY</strong> are all used to define functions with the __stdcall calling convention.</span></span> <span data-ttu-id="d6ac8-886">La plupart des fonctions de l’API Windows sont déclarées à l’aide de <strong>WinAPI</strong>.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-886">Most functions in the Windows API are declared using <strong>WINAPI</strong>.</span></span> <span data-ttu-id="d6ac8-887">Vous pouvez utiliser le <strong>rappel</strong> pour les fonctions de rappel que vous implémentez pour aider à identifier la fonction en tant que fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-887">You may wish to use <strong>CALLBACK</strong> for the callback functions that you implement to help identify the function as a callback function.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6ac8-888"><span id="WORD"></span><span id="word"></span><strong>AUTOMATIQUE</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-888"><span id="WORD"></span><span id="word"></span><strong>WORD</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-889">Entier non signé 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-889">A 16-bit unsigned integer.</span></span> <span data-ttu-id="d6ac8-890">La plage est comprise entre 0 et 65535 décimale.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-890">The range is 0 through 65535 decimal.</span></span></p>
<p><span data-ttu-id="d6ac8-891">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-891">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned short WORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6ac8-892"><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></span><span class="sxs-lookup"><span data-stu-id="d6ac8-892"><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></span></span></td>
<td><p><span data-ttu-id="d6ac8-893">Paramètre de message.</span><span class="sxs-lookup"><span data-stu-id="d6ac8-893">A message parameter.</span></span></p>
<p><span data-ttu-id="d6ac8-894">Ce type est déclaré dans WinDef. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="d6ac8-894">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UINT_PTR WPARAM;</code></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="d6ac8-895">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6ac8-895">Requirements</span></span>



| <span data-ttu-id="d6ac8-896">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6ac8-896">Requirement</span></span> | <span data-ttu-id="d6ac8-897">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6ac8-897">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6ac8-898">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6ac8-898">Minimum supported client</span></span><br/> | <span data-ttu-id="d6ac8-899">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6ac8-899">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="d6ac8-900">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6ac8-900">Minimum supported server</span></span><br/> | <span data-ttu-id="d6ac8-901">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6ac8-901">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                |
| <span data-ttu-id="d6ac8-902">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6ac8-902">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6ac8-903"><dt>BaseTsd. h ; </dt> <dt>WinDef. h ; </dt> <dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6ac8-903"><dt>BaseTsd.h; </dt> <dt>WinDef.h; </dt> <dt>WinNT.h</dt></span></span> </dl> |
