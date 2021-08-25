---
title: À propos de strsafe. h
description: Une mauvaise gestion de la mémoire tampon est impliquée dans de nombreux problèmes de sécurité qui impliquent des dépassements de mémoire tampon.
ms.assetid: a104a260-1edb-441a-acf8-e2bd3a7d8235
keywords:
- fonctions de chaîne
- Strsafe. h
- Fonctions strsafe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb5d50a6921e2775c64fd4db53393332c667aba975ffa366fb2eb49881b6beaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720589"
---
# <a name="about-strsafeh"></a>À propos de strsafe. h

Une mauvaise gestion de la mémoire tampon est impliquée dans de nombreux problèmes de sécurité qui impliquent des dépassements de mémoire tampon. Les fonctions définies dans strsafe. h fournissent un traitement supplémentaire pour la gestion correcte de la mémoire tampon dans votre code. pour cette raison, ils sont destinés à remplacer leurs équivalents C/C++ intégrés, ainsi que les implémentations de Windows spécifiques. Strsafe. h est disponible dans le SDK Windows à partir de Windows XP avec Service Pack 2 (SP2).

Les avantages des fonctions strsafe sont les suivants :

-   La taille de la mémoire tampon de destination est toujours fournie à la fonction pour garantir que la fonction n’écrit pas au-delà de la fin de la mémoire tampon.

-   Il est garanti que les tampons se terminent par un caractère null, même si l’opération tronque le résultat prévu.

-   Toutes les fonctions retournent une valeur **HRESULT** , avec un seul code de réussite possible (**S \_ OK**).

-   Chaque fonction est disponible dans une version de nombre de caractères (« CCH ») ou de nombre d’octets (« CB ») correspondante.

-   La plupart des fonctions ont une version étendue (« ex ») disponible pour les fonctionnalités avancées.

Pour plus d’informations, consultez les sections suivantes.

-   [Fonctions de nombre de caractères](#character-count-functions)
-   [Fonctions de nombre d’octets](#byte-count-functions)
-   [Utilisation de strsafe. h](#using-strsafeh)
-   [Rubriques connexes](#related-topics)

## <a name="character-count-functions"></a>Fonctions de nombre de caractères

Les fonctions suivantes utilisent un nombre de caractères plutôt qu’un nombre d’octets.



| Fonction                                                                                                                                                                                                                      | Remplace                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>[**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)</dt> <dt> [ **StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)</dt> </dl>                 | <dl> <dt>[strcat, wcscat, \_ tcsat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019)</dt> <dt>[**lstrcat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata)</dt> <dt>[**strcat**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatw)</dt> <dt>[**StrCatBuff**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatbuffa)</dt> </dl>                                                                             |
| <dl> <dt>[**StringCchCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)</dt> <dt> [ **StringCchCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)</dt> </dl>             | <dl> <dt>[strncat](/cpp/c-runtime-library/reference/strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l?view=vs-2019)</dt> <dt> [ **strncat**](/windows/desktop/api/shlwapi/nf-shlwapi-strncata)</dt> </dl>                                                                                                                                                                                                                                                                   |
| <dl> <dt>[**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)</dt> <dt> [ **StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)</dt> </dl>             | <dl> <dt>[strcpy, wcscpy, \_ tcscpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019)</dt> <dt>[**lstrcpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya)</dt> <dt>[**strcpy**](/windows/desktop/api/shlwapi/nf-shlwapi-strcpyw)</dt> </dl>                                                                                                                                                                    |
| <dl> <dt>[**StringCchCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)</dt> <dt> [ **StringCchCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)</dt> </dl>         | <dl> <dt>[strncpy, wcsncpy, \_ tcsncpy](/cpp/c-runtime-library/reference/strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>[**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)</dt> <dt> [ **StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)</dt> </dl>             | <dl> <dt>[Obtient, \_ getws, \_ Getts](/cpp/c-runtime-library/gets-getws?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>[**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)</dt> <dt> [ **StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)</dt> </dl>     | <dl> <dt>[sprintf, swprintf, \_ stprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)</dt> <dt>[**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)</dt> <dt>[**wnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wnsprintfa)</dt> <dt>[ \_ snprintf, \_ snwprintf, \_ sntprintf](/cpp/c-runtime-library/reference/snprintf-snprintf-snprintf-l-snwprintf-snwprintf-l?view=vs-2019)</dt> </dl>          |
| <dl> <dt>[**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)</dt> <dt> [ **StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)</dt> </dl> | <dl> <dt>[vsprintf, vswprintf, \_ vstprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019)</dt> <dt>[vsnprintf, \_ vsnwprintf, \_ vsntprintf](/cpp/c-runtime-library/reference/vsnprintf-vsnprintf-vsnprintf-l-vsnwprintf-vsnwprintf-l?view=vs-2019)</dt> <dt>[**Wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa)</dt> <dt>[**wvnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wvnsprintfa)</dt> </dl>, |
| <dl> <dt>[**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)</dt> </dl>                                                                                                         | <dl> <dt>[strlen, wcslen, \_ tcslen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="byte-count-functions"></a>Fonctions de nombre d’octets

Les fonctions suivantes utilisent un nombre d’octets plutôt qu’un nombre de caractères.



| Fonction                                                                                                                                                                                                                  | Remplace                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>[**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)</dt> <dt> [ **StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)</dt> </dl>                 | <dl> <dt>[strcat, wcscat, \_ tcsat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019)</dt> <dt>[**lstrcat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata)</dt> <dt>[**strcat**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatw)</dt> <dt>[**StrCatBuff**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatbuffa)</dt> </dl>                                                                            |
| <dl> <dt>[**StringCbCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)</dt> <dt> [ **StringCbCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)</dt> </dl>             | <dl> <dt>[strncat](/cpp/c-runtime-library/reference/strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l?view=vs-2019)</dt> <dt> [ **strncat**](/windows/desktop/api/shlwapi/nf-shlwapi-strncata)</dt> </dl>                                                                                                                                                                                                                                                                  |
| <dl> <dt>[**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)</dt> <dt> [ **StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)</dt> </dl>             | <dl> <dt>[strcpy, wcscpy, \_ tcscpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019)</dt> <dt>[**lstrcpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya)</dt> <dt>[**strcpy**](/windows/desktop/api/shlwapi/nf-shlwapi-strcpyw)</dt> </dl>                                                                                                                                                                   |
| <dl> <dt>[**StringCbCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)</dt> <dt> [ **StringCbCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)</dt> </dl>         | <dl> <dt>[strncpy, wcsncpy, \_ tcsncpy](/cpp/c-runtime-library/reference/strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>[**StringCbGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)</dt> <dt> [ **StringCbGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)</dt> </dl>             | <dl> <dt>[Obtient, \_ getws, \_ Getts](/cpp/c-runtime-library/gets-getws?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>[**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)</dt> <dt> [ **StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)</dt> </dl>     | <dl> <dt>[sprintf, swprintf, \_ stprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)</dt> <dt>[**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)</dt> <dt>[**wnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wnsprintfa)</dt> <dt>[ \_ snprintf, \_ snwprintf, \_ sntprintf](/cpp/c-runtime-library/reference/snprintf-snprintf-snprintf-l-snwprintf-snwprintf-l?view=vs-2019)</dt> </dl>         |
| <dl> <dt>[**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)</dt> <dt> [ **StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)</dt> </dl> | <dl> <dt>[vsprintf, vswprintf, \_ vstprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019)</dt> <dt>[vsnprintf, \_ vsnwprintf, \_ vsntprintf](/cpp/c-runtime-library/reference/vsnprintf-vsnprintf-vsnprintf-l-vsnwprintf-vsnwprintf-l?view=vs-2019)</dt> <dt>[**Wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa)</dt> <dt>[**wvnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wvnsprintfa)</dt> </dl> |
| <dl> <dt>[**StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)</dt> </dl>                                                                                                       | <dl> <dt>[strlen, wcslen, \_ tcslen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="using-strsafeh"></a>Utilisation de strsafe. h

-   Pour utiliser les fonctions strsafe Inline, incluez le fichier d’en-tête comme indiqué ici, en suivant les instructions **\# include** pour tous les autres fichiers d’en-tête.

    `#include <strsafe.h>`

-   Pour utiliser le formulaire fonctions dans la bibliothèque, incluez l’instruction suivante avant d’inclure strsafe. h. Toutefois, il est recommandé d’utiliser les fonctions inline.

    `#define STRSAFE_LIB`

    > [!Note]  
    > : Les fonctions suivantes doivent être utilisées en tant que fonctions inline : [**StringCbGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa), [**StringCbGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa), [**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)et [**StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa).

     

-   Lorsque vous incluez strsafe. h dans votre fichier, les fonctions antérieures remplacées par les fonctions strsafe. h seront dépréciées. Toute tentative d’utilisation de ces fonctions plus anciennes entraînera une erreur du compilateur vous indiquant d’utiliser les fonctions les plus récentes. Si vous souhaitez substituer ce comportement, incluez l’instruction suivante avant d’inclure strsafe. h.

    `#define STRSAFE_NO_DEPRECATE`

-   Pour autoriser uniquement les fonctions de nombre de caractères, ajoutez l’instruction suivante avant d’inclure strsafe. h.

    `#define STRSAFE_NO_CB_FUNCTIONS`

-   Pour n’autoriser que les fonctions de nombre d’octets, ajoutez l’instruction suivante avant d’inclure strsafe. h.

    `#define STRSAFE_NO_CCH_FUNCTIONS`

    > [!Note]  
    > Vous pouvez définir **strsafe \_ no \_ CB \_ Functions** ou **strsafe \_ no \_ CCH \_ Functions**, mais pas les deux.

     

-   Certaines fonctions strsafe ont des versions prenant en charge les paramètres régionaux. Par défaut, l’en-tête ne déclare pas ces fonctions. Pour activer ces déclarations, incluez l’instruction de macro suivante avant d’inclure strsafe. h.

    `#define STRSAFE_LOCALE_FUNCTIONS`

-   La longueur de chaîne maximale prise en charge est de 2 147 483 647 (**strsafe \_ Max \_ CCH**) caractères ANSI ou Unicode.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions strsafe](string-overviews.md)
</dt> </dl>

 

 