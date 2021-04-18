---
title: À propos des chaînes
description: Cette rubrique traite des fonctions de chaîne.
ms.assetid: f1799fbf-4619-4b19-998e-b1d2f4c19a35
keywords:
- ressources, chaînes
- chaînes
- fonctions de chaîne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff9fa6c9d93ba2f5c089b52b56816cad74bb61c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106536273"
---
# <a name="about-strings"></a>À propos des chaînes

Les fonctions de chaîne offrent aux applications la possibilité de copier, de comparer, de trier, de mettre en forme et de convertir des chaînes de caractères, ainsi que les moyens de déterminer le type de caractère de chaque caractère dans une chaîne. Toutes les fonctions de chaîne prennent en charge les jeux de caractères codés sur un octet, codés sur deux octets et Unicode si ces jeux de caractères sont pris en charge par le système d’exploitation sur lequel l’application est exécutée.

**Avertissement de sécurité :** L’utilisation incorrecte des fonctions de chaîne peut entraîner des problèmes de sécurité pour votre application. En général, cela implique un dépassement de mémoire tampon qui peut provoquer une attaque par déni de service contre votre application ou l’injection de code exécutable d’une personne malveillante. Les fonctions strsafe permettent une gestion plus sécurisée des chaînes et sont recommandées pour une meilleure sécurité pour votre application. Pour plus d’informations sur ces fonctions, consultez [utilisation des fonctions strsafe. h](strsafe-ovw.md).

Cette section décrit les rubriques suivantes.

-   [Comparaison avec les fonctions de chaîne de Run-Time C](#comparison-with-c-run-time-string-functions)
-   [Ressources de type chaîne](#string-resources)

## <a name="comparison-with-c-run-time-string-functions"></a>Comparaison avec les fonctions de chaîne de Run-Time C

De nombreuses fonctions de chaîne dupliquent ou améliorent les fonctions de chaîne familières de la bibliothèque Runtime C (CRT) standard. La plupart des améliorations permettent aux fonctions de chaîne de fonctionner avec des jeux de caractères Unicode ou étendus. Le tableau suivant répertorie les fonctions CRT, les fonctions Windows (qui prennent en charge Unicode, contrairement aux fonctions CRT) et les fonctions StrSafe.



| Fonction de chaîne CRT                                       | Fonction de chaîne Windows    | Fonction StrSafe                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [strcat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019) | [**lstrcat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata) | <dl> <dt>[**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)</dt> <dt>[**StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)</dt> <dt>[**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)</dt> <dt>[**StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)</dt> </dl>         |
| [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp?view=vs-2019) | [**lstrcmp**](/windows/desktop/api/Winbase/nf-winbase-lstrcmpa) | (aucune fonction équivalente)                                                                                                                                                                                                                                                                                                                                                                                  |
| [strcpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019) | [**lstrcpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya) | <dl> <dt>[**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)</dt> <dt>[**StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)</dt> <dt>[**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)</dt> <dt>[**StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)</dt> </dl> |
| [strlen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019) | [**lstrlen**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) | <dl> <dt>[**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)</dt> <dt> [ **StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)</dt> </dl>                                                                                                                                                                                       |



 

La fonction **strlen** , par exemple, retourne toujours le nombre d’octets dans une chaîne, mais la fonction [**lstrlen**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) retourne le nombre de valeurs **TCHAR** , qui fait référence aux octets des versions ANSI de la fonction ou des valeurs **WCHAR** pour les versions Unicode.

Les fonctions de chaîne suivantes diffèrent des fonctions C standard telles que **ToLower** et **ToUpper** en ce qu’elles opèrent sur n’importe quel caractère d’un jeu de caractères. À l’aide de la fonction [**CharLower**](/windows/desktop/api/Winuser/nf-winuser-charlowera) , par exemple, une application peut convertir un U majuscule avec un Umlaut (ü) en minuscules (ü). Pour plus d’informations sur les jeux de caractères, consultez [jeux de caractères](/windows/desktop/Intl/single-byte-character-sets)codés sur un octet.



| Fonction                               | Description                                   |
|----------------------------------------|-----------------------------------------------|
| [**CharLower**](/windows/desktop/api/Winuser/nf-winuser-charlowera)         | Convertit un caractère ou une chaîne en minuscules.  |
| [**CharLowerBuff**](/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa) | Convertit une chaîne de caractères en minuscules.     |
| [**CharNext**](/windows/desktop/api/Winuser/nf-winuser-charnexta)           | Passe au caractère suivant dans une chaîne.      |
| [**CharPrev**](/windows/desktop/api/Winuser/nf-winuser-charpreva)           | Passe au caractère précédent dans une chaîne. |
| [**CharUpper**](/windows/desktop/api/Winuser/nf-winuser-charuppera)         | Convertit un caractère ou une chaîne en majuscules.  |
| [**CharUpperBuff**](/windows/desktop/api/Winuser/nf-winuser-charupperbuffa) | Convertit une chaîne en majuscules.               |



 

Les fonctions de chaîne suivantes permettent de déterminer un caractère en fonction de la sémantique de la langue sélectionnée par l’utilisateur. Ces fonctions sont activées pour Unicode.



| Fonction                                         | Description                                     |
|--------------------------------------------------|-------------------------------------------------|
| [**IsCharAlpha**](/windows/desktop/api/Winuser/nf-winuser-ischaralphaa)               | Détermine si un caractère est alphabétique.   |
| [**IsCharAlphaNumeric**](/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica) | Détermine si un caractère est alphanumérique. |
| [**IsCharLower**](/windows/desktop/api/Winuser/nf-winuser-ischarlowera)               | Détermine si un caractère est en minuscules.    |
| [**IsCharUpper**](/windows/desktop/api/Winuser/nf-winuser-ischaruppera)               | Détermine si un caractère est en majuscules.    |



 

Le tableau suivant présente les extensions Unicode pour les fonctions runtime C (CRT) standard. Comme mentionné précédemment, les fonctions StrSafe permettent une gestion plus sûre des chaînes et sont recommandées pour une meilleure sécurité pour votre application.



| Fonction CRT standard                                       | String, fonction                | Fonction StrSafe                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [sprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)  | [**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)   | <dl> <dt>[**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)</dt> <dt>[**StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)</dt> <dt>[**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)</dt> <dt>[**StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)</dt> </dl>         |
| [vsprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019) | [**wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa) | <dl> <dt>[**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)</dt> <dt>[**StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)</dt> <dt>[**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)</dt> <dt>[**StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)</dt> </dl> |



 

## <a name="string-resources"></a>Ressources de type chaîne

Une application qui gère des chaînes de caractères dans les ressources peut être traduite dans de nouveaux langages avec un minimum d’effort. Au lieu de rechercher des chaînes dans les modules sources, vous pouvez simplement traduire les chaînes dans le fichier de ressources et relier l’application. En outre, l’utilisation de ressources de type chaîne simplifie la création de versions Unicode et non-Unicode de l’application à partir des mêmes fichiers sources.

La fonction [**LoadString**](/windows/desktop/api/Winuser/nf-winuser-loadstringa) charge une ressource de chaîne à partir du fichier exécutable d’une application. La fonction [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) charge une ressource de type chaîne et interprète les options de mise en forme qui peuvent être incorporées dans la chaîne.

Les ressources sous forme binaire sont stockées au format Unicode. Lors du chargement des ressources, les applications peuvent utiliser la version Unicode des fonctions de ressource ([**LoadStringW**](/windows/desktop/api/Winuser/nf-winuser-loadstringa), par exemple) pour obtenir des ressources en tant que données Unicode.

Pour les ressources de type chaîne 16 bits, 255 caractères correspond à la longueur maximale. Pour les ressources de type chaîne 32 bits, 65535 caractères correspond à la longueur maximale.

 

 