---
title: Types de données Windows (BaseTsd.h)
description: les types de données pris en charge par Windows sont utilisés pour définir les valeurs de retour de fonction, les paramètres de fonction et de message, ainsi que les membres de structure.
ms.assetid: 4553cafc-450e-4493-a4d4-cb6e2f274d46
keywords:
- types de données
- types de données, Windows
- API Windows
- Windows API, types de données
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
- VOID
- WCHAR
- WINAPI
- WORD
- WPARAM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3002912cafbdf2dd4fe62c19fe3faef302da8c9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008317"
---
# <a name="windows-data-types"></a>Types de données Windows

les types de données pris en charge par Windows sont utilisés pour définir les valeurs de retour de fonction, les paramètres de fonction et de message, ainsi que les membres de structure. Ils définissent la taille et la signification de ces éléments. Pour plus d’informations sur les types de données C/C++ sous-jacents, consultez [plages de types de données](/cpp/cpp/data-type-ranges?view=vs-2019).

Le tableau suivant contient les types suivants : caractère, entier, booléen, pointeur et handle. Les types caractère, entier et booléen sont communs à la plupart des compilateurs C. La plupart des noms de type pointeur commencent par le préfixe P ou LP. Les handles font référence à une ressource qui a été chargée en mémoire.

Pour plus d’informations sur la gestion des entiers 64 bits, consultez [entiers volumineux](large-integers.md).



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Type de données</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></td>
<td>Convention d’appel pour les fonctions système.<br/> Ce type est déclaré dans WinDef. h comme suit :<br/> <code>#define APIENTRY WINAPI</code><br/></td>
</tr>
<tr class="even">
<td><span id="ATOM"></span><span id="atom"></span><strong>ATOM</strong></td>
<td>Atom. Pour plus d’informations, consultez <a href="/windows/desktop/dataxchg/about-atom-tables">à propos des tables Atom</a>.<br/> Ce type est déclaré dans WinDef. h comme suit :<br/> <code>typedef WORD ATOM;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="BOOL"></span><span id="bool"></span><strong>Boolean</strong></td>
<td>Variable booléenne (doit avoir la <strong>valeur true</strong> ou <strong>false</strong>).<br/> Ce type est déclaré dans WinDef. h comme suit :<br/> <code>typedef int BOOL;</code><br/></td>
</tr>
<tr class="even">
<td><span id="BOOLEAN"></span><span id="boolean"></span><strong>EXPRESSION</strong></td>
<td>Variable booléenne (doit avoir la <strong>valeur true</strong> ou <strong>false</strong>).<br/> Ce type est déclaré dans Winnt. h comme suit :<br/> <code>typedef BYTE BOOLEAN;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="BYTE"></span><span id="byte"></span><strong>POIDS</strong></td>
<td>Octet (8 bits).<br/> Ce type est déclaré dans WinDef. h comme suit :<br/> <code>typedef unsigned char BYTE;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CALLBACK"></span><span id="callback"></span><strong>RAPPEL</strong></td>
<td>Convention d’appel pour les fonctions de rappel.<br/> Ce type est déclaré dans WinDef. h comme suit :<br/> <code>#define CALLBACK __stdcall</code><br/> Les fonctions <strong>callback</strong>, <strong>WinAPI</strong>et <strong>APIENTRY</strong> sont toutes utilisées pour définir des fonctions avec la Convention d’appel __stdcall. la plupart des fonctions de l’API Windows sont déclarées à l’aide de <strong>WINAPI</strong>. Vous pouvez utiliser le <strong>rappel</strong> pour les fonctions de rappel que vous implémentez pour aider à identifier la fonction en tant que fonction de rappel.<br/></td>
</tr>
<tr class="odd">
<td><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></td>
<td>caractère Windows (ANSI) 8 bits.<br/> Ce type est déclaré dans Winnt. h comme suit :<br/> <code>typedef char CCHAR;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CHAR"></span><span id="char"></span><strong>CHAR</strong></td>
<td>caractère Windows (ANSI) 8 bits. Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.<br/> Ce type est déclaré dans Winnt. h comme suit :<br/> <code>typedef char CHAR;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></td>
<td>Valeur de couleur rouge, vert, bleu (RVB) (32 bits). Pour plus d’informations sur ce type, consultez <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> .<br/> Ce type est déclaré dans WinDef. h comme suit :<br/> <code>typedef DWORD COLORREF;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CONST"></span><span id="const"></span><strong>CONST</strong></td>
<td>Variable dont la valeur doit rester constante pendant l’exécution. <br/> Ce type est déclaré dans WinDef. h comme suit :<br/> <code>#define CONST const</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD"></span><span id="dword"></span><strong>GRANDE</strong></td>
<td>Entier non signé 32 bits. La plage est comprise entre 0 et 4294967295 décimale.<br/> Ce type est déclaré dans IntSafe. h comme suit :<br/> <code>typedef unsigned long DWORD;</code><br/></td>
</tr>
<tr class="even">
<td><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></td>
<td>Entier 64 bits non signé. La plage est comprise entre 0 et 18446744073709551615.<br/> Ce type est déclaré dans IntSafe. h comme suit :<br/> <code>typedef unsigned __int64 DWORDLONG;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></td>
<td>Type long non signé pour la précision du pointeur. Utilisez lorsque vous effectuez un cast d’un pointeur vers un type long pour effectuer une opération arithmétique de pointeur. (Également couramment utilisé pour les paramètres 32 bits généraux qui ont été étendus à 64 bits dans les Windows 64 bits.)<br/> Ce type est déclaré dans BaseTsd. h comme suit :<br/> <code>typedef ULONG_PTR DWORD_PTR;</code><br/></td>
</tr>
<tr class="even">
<td><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></td>
<td>Entier non signé 32 bits.<br/> Ce type est déclaré dans BaseTsd. h comme suit :<br/> <code>typedef unsigned int DWORD32;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></td>
<td>Entier 64 bits non signé.<br/> Ce type est déclaré dans BaseTsd. h comme suit :<br/> <code>typedef unsigned __int64 DWORD64;</code><br/></td>
</tr>
<tr class="even">
<td><span id="FLOAT"></span><span id="float"></span><strong>DISSOCIÉ</strong></td>
<td>Variable à virgule flottante.<br/> Ce type est déclaré dans WinDef. h comme suit :<br/> <code>typedef float FLOAT;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></td>
<td>Handle d’une <a href="/windows/desktop/menurc/keyboard-accelerators">table d’accélérateurs</a>.<br/> Ce type est déclaré dans WinDef. h comme suit :<br/> <code>typedef HANDLE HACCEL;</code><br/></td>
</tr>
<tr class="even">
<td><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></td>
<td>La moitié de la taille d’un pointeur. Utilisez dans une structure qui contient un pointeur et deux petits champs.<br/> Ce type est déclaré dans BaseTsd. h comme suit :<br/> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="HANDLE"></span><span id="handle"></span><strong>TRAITÉE</strong></td>
<td><p>Handle d’un objet.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef PVOID HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></td>
<td><p>Handle d’une <a href="/windows/desktop/gdi/bitmaps">bitmap</a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HBITMAP;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></td>
<td><p>Handle d’un <a href="/windows/desktop/gdi/brushes">pinceau</a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HBRUSH;</code></p></td>
</tr>
<tr class="even">
<td><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></td>
<td><p>Handle d’un <a href="/previous-versions//dd316799(v=vs.85)">espace de couleurs</a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HCOLORSPACE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></td>
<td><p>Handle d’une conversation DDE (Dynamic Data Exchange).</p>
<p>Ce type est déclaré dans Ddeml. h comme suit :</p>
<p><code>typedef HANDLE HCONV;</code></p></td>
</tr>
<tr class="even">
<td><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></td>
<td><p>Handle d’une liste de conversations DDE.</p>
<p>Ce type est déclaré dans Ddeml. h comme suit :</p>
<p><code>typedef HANDLE HCONVLIST;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></td>
<td><p>Handle d’un <a href="/windows/desktop/menurc/cursors">curseur</a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HICON HCURSOR;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></td>
<td><p>Handle vers un <a href="/windows/desktop/gdi/device-context-types">contexte de périphérique</a> (DC).</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HDC;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></td>
<td><p>Handle vers les données DDE.</p>
<p>Ce type est déclaré dans Ddeml. h comme suit :</p>
<p><code>typedef HANDLE HDDEDATA;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></td>
<td><p>Handle d’un <a href="/windows/desktop/winstation/desktops">Bureau</a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HDESK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></td>
<td><p>Handle d’une structure de dépôt interne.</p>
<p>Ce type est déclaré dans ShellApi. h comme suit :</p>
<p><code>typedef HANDLE HDROP;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></td>
<td><p>Handle d’une structure de position de fenêtre différée.</p>
<p>Ce type est déclaré dans WinUser. h comme suit :</p>
<p><code>typedef HANDLE HDWP;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></td>
<td><p>Handle d’un <a href="/windows/desktop/gdi/metafiles">métafichier amélioré</a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HENHMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></td>
<td><p>Handle vers un fichier ouvert par <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>, et non <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef int HFILE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></td>
<td><p>Handle d’une <a href="/windows/desktop/gdi/about-fonts">police</a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HFONT;</code></p></td>
</tr>
<tr class="even">
<td><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>HGDIOBJ</strong></td>
<td><p>Handle d’un objet GDI.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HGDIOBJ;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></td>
<td><p>Handle d’un bloc de mémoire globale.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HGLOBAL;</code></p></td>
</tr>
<tr class="even">
<td><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></td>
<td><p>Handle d’un <a href="/windows/desktop/winmsg/hooks">Hook</a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HHOOK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></td>
<td><p>Handle d’une <a href="/windows/desktop/menurc/icons">icône</a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HICON;</code></p></td>
</tr>
<tr class="even">
<td><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></td>
<td><p>Handle d’une instance. Il s’agit de l’adresse de base du module en mémoire.</p>
<p><strong>HMODULE</strong> et <strong>HINSTANCE</strong> sont les mêmes aujourd’hui, mais représentaient des éléments différents en Windows 16 bits.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HINSTANCE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></td>
<td><p>Handle d’une clé de registre.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HKEY;</code></p></td>
</tr>
<tr class="even">
<td><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></td>
<td><p>Identificateur de paramètres régionaux d’entrée.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HKL;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></td>
<td><p>Handle vers un bloc de mémoire local.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HLOCAL;</code></p></td>
</tr>
<tr class="even">
<td><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></td>
<td><p>Handle d’un <a href="/windows/desktop/menurc/menus">menu</a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HMENU;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></td>
<td><p>Handle d’un <a href="/windows/desktop/gdi/metafiles">métafichier</a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></td>
<td><p>Handle d’un module. Est l’adresse de base du module en mémoire.</p>
<p><strong>HMODULE</strong> et <strong>HINSTANCE</strong> sont les mêmes dans les versions actuelles de Windows, mais représentaient des éléments différents en Windows 16 bits.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HINSTANCE HMODULE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HMONITOR"></span><span id="hmonitor"></span><strong>HMONITOR</strong></td>
<td><p>Handle d’un moniteur d’affichage.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>if(WINVER >= 0x0500) typedef HANDLE HMONITOR;</code></p></td>
</tr>
<tr class="even">
<td><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></td>
<td><p>Handle d’une palette.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HPALETTE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></td>
<td><p>Handle d’un <a href="/windows/desktop/gdi/pens">stylet</a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HPEN;</code></p></td>
</tr>
<tr class="even">
<td><span id="HRESULT"></span><span id="hresult"></span><strong>SIGNÉ</strong></td>
<td><p>Codes de retour utilisés par les interfaces COM. Pour plus d’informations, consultez <a href="/windows/desktop/com/structure-of-com-error-codes">structure des codes d’erreur com</a>. Pour tester une valeur <strong>HRESULT</strong> , utilisez les macros <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>failed</strong></a> et <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>Succeeded</strong></a> .</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef LONG HRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></td>
<td><p>Handle vers une <a href="/windows/desktop/gdi/regions">région</a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HRGN;</code></p></td>
</tr>
<tr class="even">
<td><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></td>
<td><p>Handle d’une ressource.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HRSRC;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></td>
<td><p>Handle d’une chaîne DDE.</p>
<p>Ce type est déclaré dans Ddeml. h comme suit :</p>
<p><code>typedef HANDLE HSZ;</code></p></td>
</tr>
<tr class="even">
<td><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></td>
<td><p>Handle d’une <a href="/windows/desktop/winstation/window-stations">station Windows</a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE WINSTA;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></td>
<td><p>Handle d’une <a href="/windows/desktop/winmsg/windows">fenêtre</a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE HWND;</code></p></td>
</tr>
<tr class="even">
<td><span id="INT"></span><span id="int"></span><strong>TIERS</strong></td>
<td><p>Entier signé 32 bits. La plage est comprise entre-2147483648 et 2147483647 décimal.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef int INT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></td>
<td><p>Type entier signé pour la précision du pointeur. Utilisez lorsque vous effectuez un cast d’un pointeur vers un entier pour effectuer une opération arithmétique de pointeur.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></td>
<td><p>Entier signé 8 bits.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef signed char INT8;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></td>
<td><p>Entier signé 16 bits.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef signed short INT16;</code></p></td>
</tr>
<tr class="even">
<td><span id="INT32"></span><span id="int32"></span><strong>ENTIER</strong></td>
<td><p>Entier signé 32 bits. La plage est comprise entre-2147483648 et 2147483647 décimal.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef signed int INT32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></td>
<td><p>Entier signé 64 bits. La plage est comprise entre-9223372036854775808 et 9223372036854775807 décimale.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef signed __int64 INT64;</code></p></td>
</tr>
<tr class="even">
<td><span id="LANGID"></span><span id="langid"></span><strong>LANGID</strong></td>
<td><p>Identificateur de langue. Pour plus d’informations, consultez <a href="/windows/desktop/Intl/language-identifiers">identificateurs de langue</a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef WORD LANGID;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LCID"></span><span id="lcid"></span><strong>LCID</strong></td>
<td><p>Identificateur de paramètres régionaux. Pour plus d’informations, consultez <a href="/windows/desktop/Intl/locale-identifiers">identificateurs de paramètres régionaux</a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef DWORD LCID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></td>
<td><p>Type d’informations de paramètres régionaux. Pour obtenir une liste, consultez <a href="/windows/desktop/Intl/locale-information-constants">constantes d’informations relatives aux paramètres régionaux</a>.</p>
<p>Ce type est déclaré dans WinNls. h comme suit :</p>
<p><code>typedef DWORD LCTYPE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></td>
<td><p>Identificateur du groupe de langues. Pour obtenir une liste, consultez <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales</strong></a>.</p>
<p>Ce type est déclaré dans WinNls. h comme suit :</p>
<p><code>typedef DWORD LGRPID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LONG"></span><span id="long"></span><strong>LONG</strong></td>
<td><p>Entier signé 32 bits. La plage est comprise entre-2147483648 et 2147483647 décimal.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef long LONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></td>
<td><p>Entier signé 64 bits. La plage est comprise entre-9223372036854775808 et 9223372036854775807 décimale.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></td>
<td><p>Type long signé pour la précision du pointeur. Utilisez lorsque vous effectuez un cast d’un pointeur vers un long pour effectuer une opération arithmétique de pointeur.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></td>
<td><p>Entier signé 32 bits. La plage est comprise entre-2147483648 et 2147483647 décimal.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef signed int LONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></td>
<td><p>Entier signé 64 bits. La plage est comprise entre-9223372036854775808 et 9223372036854775807 décimale.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef __int64 LONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></td>
<td><p>Paramètre de message.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef LONG_PTR LPARAM;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></td>
<td><p>Pointeur vers un <a href="#bool"><strong>booléen</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef BOOL far *LPBOOL;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></td>
<td><p>Pointeur vers un <a href="#byte"><strong>octet</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef BYTE far *LPBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></td>
<td><p>Pointeur vers une valeur <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> .</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef DWORD *LPCOLORREF;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></td>
<td><p>pointeur vers une chaîne constante se terminant par un caractère null de 8 bits Windows (ANSI). Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef __nullterminated CONST CHAR *LPCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></td>
<td><p>Un <a href="#lpcwstr"><strong>LPCWSTR</strong></a> si <strong>Unicode</strong> est défini, un <a href="#lpcstr"><strong>LPCSTR</strong></a> dans le cas contraire. pour plus d’informations, consultez <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows des Types de données pour les chaînes</a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></td>
<td><p>Pointeur vers une constante de tout type.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef CONST void *LPCVOID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></td>
<td><p>Pointeur vers une chaîne constante se terminant par null de caractères Unicode 16 bits. Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef CONST WCHAR *LPCWSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></td>
<td><p>Pointeur vers une <a href="#dword"><strong>valeur DWORD</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef DWORD *LPDWORD;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></td>
<td><p>Pointeur vers un <a href="#handle"><strong>handle</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HANDLE *LPHANDLE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></td>
<td><p>Pointeur vers un <a href="#int"><strong>entier</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef int *LPINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></td>
<td><p>Pointeur vers une <a href="#long"><strong>valeur long</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef long *LPLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></td>
<td><p>pointeur vers une chaîne se terminant par un caractère null de caractères Windows (ANSI) de 8 bits. Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef CHAR *LPSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></td>
<td><p>Un <a href="#lpwstr"><strong>LPWStr</strong></a> si <strong>Unicode</strong> est défini, sinon, <a href="#lpstr"><strong>LPSTR</strong></a> . pour plus d’informations, consultez <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows des Types de données pour les chaînes</a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></td>
<td><p>Pointeur vers n’importe quel type.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef void *LPVOID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></td>
<td><p>Pointeur vers un <a href="#word"><strong>mot</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef WORD *LPWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></td>
<td><p>Pointeur vers une chaîne se terminant par un caractère null de caractères Unicode 16 bits. Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef WCHAR *LPWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></td>
<td><p>Résultat signé du traitement du message.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef LONG_PTR LRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></td>
<td><p>Pointeur vers un <a href="#bool"><strong>booléen</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef BOOL *PBOOL;</code></p></td>
</tr>
<tr class="even">
<td><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></td>
<td><p>Pointeur vers une <a href="#boolean"><strong>valeur booléenne</strong></a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef BOOLEAN *PBOOLEAN;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></td>
<td><p>Pointeur vers un <a href="#byte"><strong>octet</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef BYTE *PBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></td>
<td><p>Pointeur vers un <a href="#char"><strong>caractère</strong></a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef CHAR *PCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></td>
<td><p>pointeur vers une chaîne constante se terminant par un caractère null de 8 bits Windows (ANSI). Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef CONST CHAR *PCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></td>
<td><p>Un <a href="#pcwstr"><strong>PCWSTR</strong></a> si <strong>Unicode</strong> est défini, un <a href="#pcstr"><strong>PCSTR</strong></a> dans le cas contraire. pour plus d’informations, consultez <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows des Types de données pour les chaînes</a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></td>
<td><p>Pointeur vers une chaîne constante se terminant par null de caractères Unicode 16 bits. Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef CONST WCHAR *PCWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></td>
<td><p>Pointeur vers une <a href="#dword"><strong>valeur DWORD</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef DWORD *PDWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></td>
<td><p>Pointeur vers un <a href="#dwordlong"><strong>DWORDLONG</strong></a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef DWORDLONG *PDWORDLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></td>
<td><p>Pointeur vers un <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef DWORD_PTR *PDWORD_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></td>
<td><p>Pointeur vers un <a href="#dword32"><strong>DWORD32</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef DWORD32 *PDWORD32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></td>
<td><p>Pointeur vers un <a href="#dword64"><strong>DWORD64</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef DWORD64 *PDWORD64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></td>
<td><p>Pointeur vers un <a href="#float"><strong>float</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef FLOAT *PFLOAT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></td>
<td><p>Pointeur vers un <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></td>
<td><p>Pointeur vers un <a href="#handle"><strong>handle</strong></a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef HANDLE *PHANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></td>
<td><p>Pointeur vers un <a href="#hkey"><strong>HKEY</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef HKEY *PHKEY;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT"></span><span id="pint"></span><strong>VIENNENT</strong></td>
<td><p>Pointeur vers un <a href="#int"><strong>entier</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef int *PINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></td>
<td><p>Pointeur vers un <a href="#int_ptr"><strong>INT_PTR</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef INT_PTR *PINT_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></td>
<td><p>Pointeur vers <a href="#int8"><strong>INT8</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef INT8 *PINT8;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></td>
<td><p>Pointeur vers un <a href="#int16"><strong>Int16</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef INT16 *PINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></td>
<td><p>Pointeur vers un <a href="#int32"><strong>Int32</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef INT32 *PINT32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></td>
<td><p>Pointeur vers un <a href="#int64"><strong>Int64</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef INT64 *PINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></td>
<td><p>Pointeur vers un <a href="#lcid"><strong>LCID</strong></a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef PDWORD PLCID;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></td>
<td><p>Pointeur vers une <a href="#long"><strong>valeur long</strong></a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef LONG *PLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONG</strong></td>
<td><p>Pointeur vers un <a href="#longlong"><strong>LongLong</strong></a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef LONGLONG *PLONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></td>
<td><p>Pointeur vers un <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef LONG_PTR *PLONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></td>
<td><p>Pointeur vers un <a href="#long32"><strong>LONG32</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef LONG32 *PLONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></td>
<td><p>Pointeur vers un <a href="#long64"><strong>LONG64</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef LONG64 *PLONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></td>
<td><p>Pointeur 32 bits. Sur un système 32 bits, il s’agit d’un pointeur natif. Sur un système 64 bits, il s’agit d’un pointeur 64 bits tronqué.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></td>
<td><p>Pointeur 64 bits. Sur un système 64 bits, il s’agit d’un pointeur natif. Sur un système 32 bits, il s’agit d’un pointeur 32 bits étendu au niveau du signe.</p>
<p>Notez qu’il n’est pas possible de supposer l’état du bit de pointeur le plus élevé.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></td>
<td><p>Pointeur signé.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>#define POINTER_SIGNED __sptr</code></p></td>
</tr>
<tr class="even">
<td><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></td>
<td><p>Pointeur non signé.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>#define POINTER_UNSIGNED __uptr</code></p></td>
</tr>
<tr class="odd">
<td><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></td>
<td><p>Pointeur vers un <a href="#short"><strong>short</strong></a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef SHORT *PSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></td>
<td><p>Pointeur vers un <a href="#size_t"><strong>size_t</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef SIZE_T *PSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></td>
<td><p>Pointeur vers un <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef SSIZE_T *PSSIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span id="PSTR"></span><span id="pstr"></span><strong>PSTR</strong></td>
<td><p>pointeur vers une chaîne se terminant par un caractère null de caractères Windows (ANSI) de 8 bits. Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef CHAR *PSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></td>
<td><p>Pointeur vers un <a href="#tbyte"><strong>to</strong></a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef TBYTE *PTBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></td>
<td><p>Pointeur vers un <a href="#tchar"><strong>TCHAR</strong></a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef TCHAR *PTCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></td>
<td><p>Un <a href="#pwstr"><strong>PWSTR</strong></a> si <strong>Unicode</strong> est défini, un <a href="#pstr"><strong>PSTR</strong></a> dans le cas contraire. pour plus d’informations, consultez <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows des Types de données pour les chaînes</a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></td>
<td><p>Pointeur vers un <a href="#uchar"><strong>UCHAR</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef UCHAR *PUCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></td>
<td><p>Pointeur vers un <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></td>
<td><p>Pointeur vers un <a href="#uint"><strong>uint</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef UINT *PUINT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></td>
<td><p>Pointeur vers un <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef UINT_PTR *PUINT_PTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></td>
<td><p>Pointeur vers <a href="#uint8"><strong>UINT8</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef UINT8 *PUINT8;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></td>
<td><p>Pointeur vers <a href="#uint16"><strong>UINT16</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef UINT16 *PUINT16;</code></p></td>
</tr>
<tr class="even">
<td><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></td>
<td><p>Pointeur vers un <a href="#uint32"><strong>UInt32</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef UINT32 *PUINT32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></td>
<td><p>Pointeur vers un <a href="#uint64"><strong>UINT64</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef UINT64 *PUINT64;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></td>
<td><p>Pointeur vers un <a href="#ulong"><strong>ULong</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef ULONG *PULONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></td>
<td><p>Pointeur vers un <a href="#ulonglong"><strong>ULONGLONG</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef ULONGLONG *PULONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></td>
<td><p>Pointeur vers un <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef ULONG_PTR *PULONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></td>
<td><p>Pointeur vers un <a href="#ulong32"><strong>ULONG32</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef ULONG32 *PULONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></td>
<td><p>Pointeur vers un <a href="#ulong64"><strong>ULONG64</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef ULONG64 *PULONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></td>
<td><p>Pointeur vers un <a href="#ushort"><strong>UShort</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef USHORT *PUSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PVOID"></span><span id="pvoid"></span><strong>DÉSIGNE</strong></td>
<td><p>Pointeur vers n’importe quel type.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef void *PVOID;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></td>
<td><p>Pointeur vers un <a href="#wchar"><strong>WCHAR</strong></a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef WCHAR *PWCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PWORD"></span><span id="pword"></span><strong>PWORD</strong></td>
<td><p>Pointeur vers un <a href="#word"><strong>mot</strong></a>.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef WORD *PWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></td>
<td><p>Pointeur vers une chaîne se terminant par un caractère null de caractères Unicode 16 bits. Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef WCHAR *PWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="QWORD"></span><span id="qword"></span><strong>Q</strong></td>
<td><p>Entier 64 bits non signé.</p>
<p>Ce type est déclaré comme suit :</p>
<p><code>typedef unsigned __int64 QWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></td>
<td><p>Handle d’une base de données du gestionnaire de contrôle des services. Pour plus d’informations, consultez <a href="/windows/desktop/Services/scm-handles">Handles SCM</a>.</p>
<p>Ce type est déclaré dans WinSvc. h comme suit :</p>
<p><code>typedef HANDLE SC_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></td>
<td><p>Verrou vers une base de données du gestionnaire de contrôle des services. Pour plus d’informations, consultez <a href="/windows/desktop/Services/scm-handles">Handles SCM</a>.</p>
<p>Ce type est déclaré dans WinSvc. h comme suit :</p>
<p><code>typedef LPVOID SC_LOCK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></td>
<td><p>Handle d’une valeur d’état de service. Pour plus d’informations, consultez <a href="/windows/desktop/Services/scm-handles">Handles SCM</a>.</p>
<p>Ce type est déclaré dans WinSvc. h comme suit :</p>
<p><code>typedef HANDLE SERVICE_STATUS_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="SHORT"></span><span id="short"></span><strong>Résumé</strong></td>
<td><p>Entier 16 bits. La plage est comprise entre-32768 et 32767 décimal.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef short SHORT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></td>
<td><p>Nombre maximal d’octets auxquels un pointeur peut pointer. Utilisez pour un nombre qui doit s’étendre à la plage complète d’un pointeur.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef ULONG_PTR SIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></td>
<td><p>Version signée de <a href="#size_t"><strong>size_t</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef LONG_PTR SSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span id="TBYTE"></span><span id="tbyte"></span><strong>OCTET</strong></td>
<td><p><a href="#wchar"><strong>WCHAR</strong></a> si <strong>Unicode</strong> est défini, sinon, un <a href="#char"><strong>caractère</strong></a> .</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="TCHAR"></span><span id="tchar"></span><strong>TCHAR</strong></td>
<td><p><a href="#wchar"><strong>WCHAR</strong></a> si <strong>Unicode</strong> est défini, sinon, un <a href="#char"><strong>caractère</strong></a> .</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></td>
<td><p><a href="#char"><strong>Caractère</strong></a>non signé.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef unsigned char UCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></td>
<td><p><a href="#half_ptr"><strong>HALF_PTR</strong></a>non signé. Utilisez dans une structure qui contient un pointeur et deux petits champs.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></td>
<td><p><a href="#int"><strong>Entier</strong></a>non signé. La plage est comprise entre 0 et 4294967295 décimale.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef unsigned int UINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></td>
<td><p><a href="#int_ptr"><strong>INT_PTR</strong></a>non signé.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="UINT8"></span><span id="uint8"></span><strong>DESTINÉES</strong></td>
<td><p>Unsigned <a href="#int8"><strong>INT8</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef unsigned  char UINT8;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></td>
<td><p>Unsigned <a href="#int16"><strong>Int16</strong></a>.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef unsigned  short UINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></td>
<td><p>Unsigned <a href="#int32"><strong>Int32</strong></a>. La plage est comprise entre 0 et 4294967295 décimale.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef unsigned int UINT32;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></td>
<td><p>Unsigned <a href="#int64"><strong>Int64</strong></a>. La plage est comprise entre 0 et 18446744073709551615.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef usigned __int 64 UINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="ULONG"></span><span id="ulong"></span><strong>CORRESPONDANTE</strong></td>
<td><p><a href="#long"><strong>Long</strong></a>non signé. La plage est comprise entre 0 et 4294967295 décimale.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef unsigned long ULONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></td>
<td><p>Entier 64 bits non signé. La plage est comprise entre 0 et 18446744073709551615.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></td>
<td><p><a href="#long_ptr"><strong>LONG_PTR</strong></a>non signé.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></td>
<td><p><a href="#long32"><strong>LONG32</strong></a>non signé. La plage est comprise entre 0 et 4294967295 décimale.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef unsigned int ULONG32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></td>
<td><p><a href="#long64"><strong>LONG64</strong></a>non signé. La plage est comprise entre 0 et 18446744073709551615.</p>
<p>Ce type est déclaré dans BaseTsd. h comme suit :</p>
<p><code>typedef unsigned __int64 ULONG64;</code></p></td>
</tr>
<tr class="even">
<td><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></td>
<td><p>Chaîne Unicode.</p>
<p>Ce type est déclaré dans winternl. h comme suit :</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
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
<td><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></td>
<td><p>Unsigned <a href="#short"><strong>short</strong></a>. La plage est comprise entre 0 et 65535 décimale.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef unsigned short USHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="USN"></span><span id="usn"></span><strong>NNUMÉRO</strong></td>
<td><p>Numéro de séquence de mise à jour (USN).</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef LONGLONG USN;</code></p></td>
</tr>
<tr class="odd">
<td><span id="VOID"></span><span id="void"></span><strong>NULLITÉ</strong></td>
<td><p>Tout type.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>#define VOID void</code></p></td>
</tr>
<tr class="even">
<td><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></td>
<td><p>Caractère Unicode 16 bits. Pour plus d’informations, consultez <a href="/windows/desktop/gdi/character-sets-used-by-fonts">jeux de caractères utilisés par les polices</a>.</p>
<p>Ce type est déclaré dans Winnt. h comme suit :</p>
<p><code>typedef wchar_t WCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="WINAPI"></span><span id="winapi"></span><strong>WINAPI</strong></td>
<td><p>Convention d’appel pour les fonctions système.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>#define WINAPI __stdcall</code></p>
<p>Les fonctions <strong>callback</strong>, <strong>WinAPI</strong>et <strong>APIENTRY</strong> sont toutes utilisées pour définir des fonctions avec la Convention d’appel __stdcall. la plupart des fonctions de l’API Windows sont déclarées à l’aide de <strong>WINAPI</strong>. Vous pouvez utiliser le <strong>rappel</strong> pour les fonctions de rappel que vous implémentez pour aider à identifier la fonction en tant que fonction de rappel.</p></td>
</tr>
<tr class="even">
<td><span id="WORD"></span><span id="word"></span><strong>AUTOMATIQUE</strong></td>
<td><p>Entier non signé 16 bits. La plage est comprise entre 0 et 65535 décimale.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef unsigned short WORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></td>
<td><p>Paramètre de message.</p>
<p>Ce type est déclaré dans WinDef. h comme suit :</p>
<p><code>typedef UINT_PTR WPARAM;</code></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                                                                                                                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>BaseTsd. h ; </dt> <dt>WinDef. h ; </dt> <dt>Winnt. h</dt> </dl> |
