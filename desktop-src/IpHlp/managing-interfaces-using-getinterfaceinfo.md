---
description: La fonction GetInterfaceInfo remplit un pointeur vers une structure d’informations d' \_ interface IP \_ avec des informations sur les interfaces associées au système.
ms.assetid: 0cc18e14-7329-49b0-bb07-912fa403db46
title: Gestion des interfaces à l’aide de GetInterfaceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cc2afa6fe0b520e1cc5f952b44bc94052b630f4335bd739b4d7c3582d16e277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146742"
---
# <a name="managing-interfaces-using-getinterfaceinfo"></a>Gestion des interfaces à l’aide de GetInterfaceInfo

La fonction [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) remplit un pointeur vers une structure d’informations d' [**\_ interface \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) avec des informations sur les interfaces associées au système.

**Pour utiliser GetInterfaceInfo**

1.  Déclarez un pointeur vers un objet d' [**\_ \_ informations d’interface IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) appelé `pInfo` , et un objet **ULong** appelé `ulOutBufLen` . Déclarez également un objet **DWORD** appelé `dwRetVal` (utilisé pour la vérification des erreurs).
    ```C++
        ULONG               ulOutBufLen;
        DWORD               dwRetVal;
        unsigned int       i;

        IP_INTERFACE_INFO*  pInterfaceInfo;
    ```

    

2.  Allouez de la mémoire pour les structures.
    > [!Note]  
    > La taille de `ulOutBufLen` n’est pas suffisante pour contenir les informations. Consultez l’étape suivante.

     

    ```C++
        pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(sizeof (IP_INTERFACE_INFO));
        ulOutBufLen = sizeof(IP_INTERFACE_INFO);
    
    ```

    

3.  Effectuez un appel initial à [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) pour connaître la taille nécessaire à la `ulOutBufLen` variable.
    > [!Note]  
    > Cet appel à la fonction est censé échouer et est utilisé pour s’assurer que la `ulOutBufLen` variable spécifie une taille suffisante pour contenir toutes les informations retournées à `pInfo` . Il s’agit d’un modèle de programmation commun dans le programme d’assistance IP pour les structures de données et les fonctions de ce type.

     

    ```C++
        if (GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen) ==
            ERROR_INSUFFICIENT_BUFFER) {
            free(pInterfaceInfo);
            pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(ulOutBufLen);
        }
    ```

    

4.  Effectuez un deuxième appel à [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) avec une vérification d’erreur générale et retournez sa valeur à la variable **DWORD** `dwRetVal` (pour une vérification des erreurs plus avancée).
    ```C++
        if ((dwRetVal = GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen)) != NO_ERROR) {
            printf("  GetInterfaceInfo failed with error: %d\n", dwRetVal);
        }
    ```

    

5.  Si l’appel a réussi, accédez aux données de la `pInfo` structure de données.

    ```C++
            printf("  GetInterfaceInfo succeeded.\n");

            printf("  Num Adapters: %ld\n\n", pInterfaceInfo->NumAdapters);
            for (i = 0; i < (unsigned int) pInterfaceInfo->NumAdapters; i++) {
                printf("  Adapter Index[%d]: %ld\n", i,
                       pInterfaceInfo->Adapter[i].Index);
                printf("  Adapter Name[%d]:  %ws\n\n", i,
                       pInterfaceInfo->Adapter[i].Name);
            }
        }
    ```

    

    > [!Note]  
    > Le% WS de la première ligne indique une chaîne étendue. Cela est utilisé, car l’attribut **Name** de la structure de mappage d’index de la [**\_ carte \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` est **WCHAR**, qui est une chaîne Unicode.

     

6.  Libérez la mémoire allouée pour la structure *pinfo* .
    ```C++
        if (pInterfaceInfo) {
            free(pInterfaceInfo);
            pInterfaceInfo = NULL;
        }
    ```

    

Étape suivante : [gestion des adresses IP à l’aide de GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)

Étape précédente : [gestion des cartes réseau à l’aide de GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)

 

 



