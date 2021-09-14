---
description: Votre application peut prendre en charge un autre ensemble de langues d’interface utilisateur que celles prises en charge par le système d’exploitation cible. Cette rubrique décrit ce type de prise en charge, à l’aide d’extraits de code complets.
ms.assetid: cb9f2a5f-3bb8-4287-a542-c71d20b37194
title: prise en charge du langage de Application-Specific Paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6bddfe94586751d3b0f4757c670c006317e49b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121838"
---
# <a name="supporting-application-specific-language-settings"></a>prise en charge du langage de Application-Specific Paramètres

Votre application peut prendre en charge un autre ensemble de langues d’interface utilisateur que celles prises en charge par le système d’exploitation cible. Cette rubrique décrit ce type de prise en charge, à l’aide d’extraits de code complets.

## <a name="interpret-users-language-preference"></a>Interpréter la préférence de langue de l’utilisateur

Votre application doit d’abord déterminer la langue de l’interface utilisateur à afficher, en fonction de la préférence de l’utilisateur. Le code peut lire les paramètres à partir d’un fichier de configuration ou des paramètres du Registre.

L’exemple suivant définit deux fonctions utilisées pour interpréter la préférence de langue de l’utilisateur. La première fonction illustre la lecture d’une liste délimitée de langues à partir d’un fichier, représentée dans le code sous la forme « langs.txt ». Les délimiteurs pris en charge dans l’exemple sont « , », « ; », « . » et «». La deuxième fonction convertit la chaîne lue à partir du fichier en une valeur de chaînes multiples. Cette opération est nécessaire, car les fonctions MUI utilisées pour définir des langages acceptent uniquement des valeurs à chaînes multiples.


```C++
BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
{
    BOOL rtnVal = FALSE;
    // Very simple implementation - assumes that first 'langStrSize' characters of the
    // L".\\langs.txt" file comprises a string of one or more languages.
    HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0,
                                    NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    if(langConfigFileHandle != INVALID_HANDLE_VALUE)
    {
        // Clear the input variables.
        DWORD bytesActuallyRead = 0;
        if(ReadFile(langConfigFileHandle, langStr, langStrSize*sizeof(WCHAR), &bytesActuallyRead, NULL)
           && bytesActuallyRead > 0)
        {
            rtnVal = TRUE;
            DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize)
                              ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
            langStr[nullIndex] = L'\0';
        }
        CloseHandle(langConfigFileHandle);
    }
    return rtnVal;
}
BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
{
    BOOL rtnVal = FALSE;
    size_t strLen = 0;
    rtnVal = SUCCEEDED(StringCchLengthW(langStr, USER_CONFIGURATION_STRING_BUFFER*2, &strLen));
    if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
    {
        WCHAR * langMultiStrPtr = langMultiStr;
        WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
        WCHAR * context = last;
        WCHAR * next = wcstok_s(last,L",; :",&context);
        while(next && rtnVal)
        {
            // Make sure you validate the user input.
            if(SUCCEEDED(StringCchLengthW(last, LOCALE_NAME_MAX_LENGTH, &strLen))
               && IsValidLocaleName(next))
            {
                langMultiStrPtr[0] = L'\0';
                rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,
                                    (langMultiStrSize - (langMultiStrPtr - langMultiStr)), next));
                langMultiStrPtr += strLen + 1;
            }
            next = wcstok_s(NULL, L",; :", &context);
            if(next)
                last = next;
        }
        // Make sure there is a double null term for the multi-string.
        if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr)))
        {
            langMultiStrPtr[0] = L'\0';
        }
        else // Fail and guard anyone whom might use the multi-string.
        {
            langMultiStr[0] = L'\0';
            langMultiStr[1] = L'\0';
        }
    }
    return rtnVal;
}
```



## <a name="set-the-application-language"></a>Définir la langue de l’application

Après avoir lu les informations de préférence de langue, le code de l’application doit utiliser le paramètre récupéré pour définir la langue de l’application. sur Windows 7 et versions ultérieures, l’application peut définir la langue au niveau du processus en appelant la fonction [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) .


```C++
DWORD langCount = 0;
// Using SetProcessPreferredUILanguages is recommended for new applications (esp. multi-threaded applications).
if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME, userLanguagesMultiString, &langCount) || langCount == 0)
{
    swprintf_s(displayBuffer, SUFFICIENTLY_LARGE_ERROR_BUFFER,
               L"FAILURE: Unable to set the user defined languages, last error = %d.", GetLastError());
    MessageBoxW(NULL, displayBuffer, L"HelloMUI ERROR!", MB_OK | MB_ICONERROR);
    return 1; // Exit.
}
```



sur Windows Vista et versions ultérieures, la langue de l’application est définie au niveau du thread en appelant la fonction [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) .


```C++
DWORD langCount = 0;
// The following line of code is supported on Windows Vista and later.
if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME, userLanguagesMultiString, &langCount) || langCount == 0)
{
    swprintf_s(displayBuffer, SUFFICIENTLY_LARGE_ERROR_BUFFER,
               L"FAILURE: Unable to set the user defined languages, last error = %d.", GetLastError());
    MessageBoxW(NULL, displayBuffer, L"HelloMUI ERROR!", MB_OK | MB_ICONERROR);
    return 1; // Exit.
}
return 1;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition des préférences linguistiques de l’application](setting-application-language-preferences.md)
</dt> <dt>

[MUI : exemple de Paramètres Application-Specific (Windows Vista)](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[MUI : exemple de Paramètres Application-Specific (pré-Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 



