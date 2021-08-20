---
description: La \_ notification SPFILENOTIFY QUEUESCAN \_ signataires est envoyée à une routine de rappel par SetupScanFileQueue pour chaque nœud dans la sous-file d’attente de copie de la file d’attente de fichiers.
ms.assetid: 5b22e8ba-9a18-461b-bad7-b2d76f83d7f3
title: Message d’SPFILENOTIFY_QUEUESCAN_SIGNERINFO (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33e448178629dd9c4528fbc0257a7ceed79b7bf7dc6e6c2d70e631e2c3bd1cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964413"
---
# <a name="spfilenotify_queuescan_signerinfo-message"></a>\_Message SPFILENOTIFY QUEUESCAN \_ signataires

La notification **SPFILENOTIFY \_ QUEUESCAN \_ signataires** est envoyée à une routine de rappel par [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) pour chaque nœud dans la sous-file d’attente de copie de la file d’attente de fichiers. Cela se produit uniquement si la fonction **SetupScanFileQueue** a été appelée en spécifiant le rappel d’utilisation de l’indicateur SPQ \_ Scan \_ \_ \_ signataires. disponible à partir de Windows XP.


```C++
SPFILENOTIFY_QUEUESCAN_SIGNERINFO
  Param1 = (PFILEPATHS_SIGNERINFO) Filepaths;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Pointeur vers une structure [**FILEPATHS \_ signataires**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) . Le membre **cible** est le nom du fichier cible sur le système. Le membre **source** est le chemin d’accès attendu du fichier source. Le membre **Win32Error** est l’erreur de signature. Les informations de signature sont retournées si la routine de rappel retourne **Win32Error**= = no \_ Error. Le membre **DigitalSigner** est le signataire numérique. Le membre **version** est la version. **CatalogFile** est le fichier catalogue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La routine de rappel doit retourner un [code d’erreur système](/windows/desktop/Debug/system-error-codes).

Si la routine de rappel ne retourne aucune \_ erreur, l’analyse de la file d’attente continue et retourne si la routine retourne un autre code d’erreur, l’analyse de la file d’attente s’interrompt et [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) retourne la **valeur false**.

> [!Note]  
> Cette notification n’est pas gérée par la fonction [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .

 

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d'ensemble](overview.md)
</dt> <dt>

[Notifications](notifications.md)
</dt> <dt>

[**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

