---
title: Prise en charge des IDN dans WinINet
description: À compter de Windows Server 2008 et Windows Vista, la partie hôte de l’URL Unicode est convertie en nom de domaine international (IDN, Internationalized Domain Name).
ms.assetid: 7c56908e-f6d0-48dc-9ac1-73f888fb7b6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510b1bc8d2ab77534d7f5dac587f287d5e7095af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382591"
---
# <a name="idn-support-in-wininet"></a>Prise en charge des IDN dans WinINet

À compter de Windows Server 2008 et Windows Vista, la partie hôte de l’URL Unicode est convertie en nom de domaine international (IDN, Internationalized Domain Name). Des parties distinctes de l’encodage d’URL Unicode peuvent également être modifiées par des configurations définies par l’application. Les versions ANSI de l’API WinINet continuent à envoyer l’URL sur le réseau telle qu’elle est entrée par l’application. Toutefois, les versions Unicode WinINet de l’API sont désormais conformes à la norme IDN (RFC3490) pour les encodages d’URL.

Par défaut, lorsqu’une URL est entrée en tant que paramètre Unicode, la partie hôte, pour les connexions proxy et directes, est convertie au format IDN. L’application a la possibilité de désactiver la mise en forme de l’hôte IDN en définissant l’option **Internet \_ \_ IDN** . La conversion de l’hôte IDN peut être activée uniquement sur les connexions directes ou proxy à l’aide de l’indicateur Internet indicateurs de **\_ \_ \_ proxy** IDN **\_ \_ \_ direct** ou Internet indicateur IDN avec l' **\_ option Internet \_ IDN**.

L’exemple de code suivant montre comment désactiver la conversion de l’hôte IDN à la fois pour le proxy et pour les connexions directes.

``` syntax
DWORD IDN = 0; 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_IDN,
                   &IDN, 
                   sizeof(DWORD) ); 
```

Si la mise en forme de l’hôte IDN est désactivée, l’application a la possibilité de spécifier la page de codes souhaitée à l’aide de la **\_ page de \_ codes d’option Internet**.

L’exemple de code suivant montre comment spécifier la page de codes japonaise.

``` syntax
DWORD CP_SHIFT_JIS = 932;  // ANSI/OEM  Japanese, Shift-JIS
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE,
                   &CP_SHIFT_JIS, 
                   Sizeof(DWORD) ); 
```

La partie du chemin d’accès de l’URL est encodée en UTF8 par défaut, et les autres segments de l’URL, la requête ou le fragment, sont convertis en page de codes système par défaut (CP \_ ACP).

L’exemple suivant montre comment spécifier la page de codes de langue coréenne pour la partie chemin d’accès de l’URL.

``` syntax
DWORD CP_KOREAN = 949;   // ANSI/OEM Korean 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE_PATH,
                   &CP_KOREAN, 
                   sizeof(DWORD) );
```

Le tableau suivant définit les options qui prennent en charge l’IDN. Pour plus d’informations, consultez la rubrique [indicateurs d’option](option-flags.md) .



| Option                            | Description                                                                                                                                                                                                                     |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| page de codes de l' \_ option Internet \_        | Cette option est définie sur la demande, ou sur le descripteur de connexion, pour spécifier un schéma d’encodage de page de codes pour la partie hôte de l’URL. Cette option est ignorée si l’IDN est activé.                                                      |
| chemin de la page de codes de l' \_ option Internet \_ \_  | Cette option est définie sur la demande, ou le descripteur de connexion active le schéma d’encodage spécifié pour la partie chemin d’accès de l’URL. Par défaut, la partie chemin d’accès de l’URL est encodée en UTF8.                                         |
| page de codes de l' \_ option Internet \_ \_ extra | La définition de cette option sur la demande, ou le descripteur de connexion active le schéma d’encodage spécifié pour la partie supplémentaire de l’URL. Par défaut, la partie supplémentaire de l’URL est encodée dans la page de codes système par défaut (CP \_ ACP). |
| \_IDN des options Internet \_             | Cette option peut être utilisée sur la demande ou sur le descripteur de connexion pour activer ou désactiver la conversion de l’hôte IDN. Lorsque l’IDN est désactivé, WinINet utilise la page de codes par défaut du système pour encoder la partie hôte ou autorité de l’URL.       |



 

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 