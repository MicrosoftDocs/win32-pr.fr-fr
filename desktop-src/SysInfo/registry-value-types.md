---
description: Une valeur de Registre peut stocker des données dans différents formats.
ms.assetid: 5fd828d6-4d62-4823-a2f1-15782b5cd28c
title: Types de valeur de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc653e69c514bc77323704485e88f0a57eebaae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865701"
---
# <a name="registry-value-types"></a>Types de valeur de Registre

Une valeur de Registre peut stocker des données dans différents formats. Lorsque vous stockez des données sous une valeur de Registre, par exemple en appelant la fonction [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) , vous pouvez spécifier l’une des valeurs suivantes pour indiquer le type de données stockées. Lorsque vous récupérez une valeur de Registre, les fonctions telles que [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) utilisent ces valeurs pour indiquer le type de données récupérées.

Les types de valeurs de registre suivants sont définis dans Winnt. h.



| Valeur                                 | Type                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_fichier binaire reg<br/>                | Données binaires dans tout formulaire.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| \_valeur DWORD reg<br/>                 | Nombre de 32 bits.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| REG \_ DWORD \_ Little \_ ENDIAN<br/> | Nombre 32 bits au format avec primauté des octets de poids faible (Little endian).<br/> Windows est conçu pour s’exécuter sur des architectures d’ordinateur Little-endian. Par conséquent, cette valeur est définie en tant que REG \_ DWORD dans les fichiers d’en-tête Windows.<br/>                                                                                                                                                                                                                          |
| REG \_ DWORD \_ Big \_ ENDIAN<br/>    | Nombre 32 bits au format Big-endian.<br/> Certains systèmes UNIX prennent en charge les architectures de Big-endian.<br/>                                                                                                                                                                                                                                                                                                                         |
| REG \_ développer \_ SZ<br/>            | Chaîne terminée par le caractère null qui contient des références non développées à des variables d’environnement (par exemple, "% PATH%"). Il s’agit d’une chaîne Unicode ou ANSI selon que vous utilisez les fonctions Unicode ou ANSI. Pour développer les références de variable d’environnement, utilisez la fonction [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) .<br/>                                                                                 |
| \_lien reg<br/>                  | Chaîne Unicode terminée par le caractère null qui contient le chemin d’accès cible d’un lien symbolique qui a été créé en appelant la fonction [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) avec l’option de création de la \_ commande reg \_ \_ .<br/>                                                                                                                                                                                                                          |
| REG \_ multiple \_ SZ<br/>             | Séquence de chaînes se terminant par un caractère null, terminée par une chaîne vide ( \\ 0).<br/> Par exemple :<br/> *Chaîne1* \\ 0 *Chaîne2* \\ 0 *string3* \\ 0 *LastString* \\ 0 \\ 0<br/> Le premier \\ 0 termine la première chaîne, la seconde jusqu’au dernier \\ 0 termine la dernière chaîne, et le \\ 0 final termine la séquence. Notez que la marque de fin finale doit être factorisée dans la longueur de la chaîne.<br/> |
| REG \_ aucun<br/>                  | Aucun type valeur défini.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_q QWord<br/>                 | Nombre de 64 bits.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ faible primauté des \_ octets de poids faible<br/> | Nombre 64 bits au format avec primauté des octets de poids faible (Little endian).<br/> Windows est conçu pour s’exécuter sur des architectures d’ordinateur Little-endian. Par conséquent, cette valeur est définie sous \_ la forme reg QWord dans les fichiers d’en-tête Windows.<br/>                                                                                                                                                                                                                          |
| SZ de REG \_<br/>                    | Chaîne se terminant par une valeur null. Il s’agit d’une chaîne Unicode ou ANSI, selon que vous utilisez les fonctions Unicode ou ANSI.<br/>                                                                                                                                                                                                                                                                                       |



 

## <a name="string-values"></a>Valeurs de type chaîne

Si les données ont le \_ type reg SZ, reg \_ \_ multisz ou reg \_ expand \_ SZ, la chaîne n’a peut-être pas été stockée avec les caractères null de fin appropriés. Par conséquent, lors de la lecture d’une chaîne à partir du Registre, vous devez vous assurer que la chaîne se termine correctement avant de l’utiliser. Sinon, elle peut remplacer une mémoire tampon. (Notez que REG \_ Les \_ chaînes à plusieurs SZ doivent avoir deux caractères null de fin.)

Lors de l’écriture d’une chaîne dans le registre, vous devez spécifier la longueur de la chaîne, y compris le caractère null de fin ( \\ 0). Une erreur courante consiste à utiliser la fonction **strlen** pour déterminer la longueur de la chaîne, mais d’oublier que **strlen** retourne uniquement le nombre de caractères de la chaîne, à l’exclusion de la valeur null de fin. Par conséquent, la longueur de la chaîne doit être calculée comme suit : `strlen( string ) + 1`

Une \_ \_ chaîne à plusieurs SZS reg se termine par une chaîne de longueur 0. Par conséquent, il n’est pas possible d’inclure une chaîne de longueur nulle dans la séquence. Une séquence vide est définie comme suit : \\ 0.

L’exemple suivant parcourt \_ une \_ chaîne reg multiple sz.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

void SampleSzz(PTSTR pszz)
{
   _tprintf(_TEXT("\tBegin multi-sz string\n"));
   while (*pszz) 
   {
      _tprintf(_TEXT("\t\t%s\n"), pszz);
      pszz = pszz + _tcslen(pszz) + 1;
   }
   _tprintf(_TEXT("\tEnd multi-sz\n"));
}

int __cdecl main(int argc, char **argv)
{
   // Because the compiler adds a \0 at the end of quoted strings, 
   // there are two \0 terminators at the end. 

   _tprintf(_TEXT("Conventional multi-sz string:\n"));  
   SampleSzz(_TEXT("String1\0String2\0String3\0LastString\0"));

   _tprintf(_TEXT("\nTest case with no strings:\n"));  
   SampleSzz(_TEXT(""));

   return 0;
}
```



## <a name="byte-formats"></a>Formats d’octets

Dans un format avec primauté des octets de poids faible ( *Little-endian*), une valeur multioctet est stockée en mémoire à partir de l’octet le plus bas (le « petit end ») jusqu’à l’octet le plus élevé. Par exemple, la valeur 0x12345678 sinon est stockée sous la forme (0x78 0x56 0x34 0x12) au format avec primauté des octets de poids faible (Little endian).

Au *format Big-endian*, une valeur sur plusieurs octets est stockée en mémoire à partir de l’octet le plus élevé (le « Big end ») jusqu’à l’octet le plus bas. Par exemple, la valeur 0x12345678 sinon est stockée sous la forme (0x12 0x34 0x56 0x78) au format Big-endian.

 

