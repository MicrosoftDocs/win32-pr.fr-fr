---
description: La \_ notification SPFILENOTIFY FILEOPDELAYED est envoyée par SetupInstallFileEx ou SetupCommitFileQueue à une routine de rappel lorsqu’une opération de fichier a été retardée parce que le fichier était en cours d’utilisation. L’opération sera traitée lors du prochain redémarrage du système.
ms.assetid: a0b38e2b-2390-49e5-b288-77c31636e696
title: Message d’SPFILENOTIFY_FILEOPDELAYED (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4c3034e7e3114bb3c55db48850cbe276c66702fc44cd67e54f0f1b47c93a2d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665099"
---
# <a name="spfilenotify_fileopdelayed-message"></a>\_Message SPFILENOTIFY FILEOPDELAYED

La notification **SPFILENOTIFY \_ FILEOPDELAYED** est envoyée par [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) ou [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) à une routine de rappel lorsqu’une opération de fichier a été retardée parce que le fichier était en cours d’utilisation. L’opération sera traitée lors du prochain redémarrage du système.


```C++
SPFILENOTIFY_FILEOPDELAYED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .

Si l’opération retardée est une opération de copie de fichier, la structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) contient les informations suivantes.



| Membre FILEPATHS | Valeur                                |
|------------------|--------------------------------------|
| **Win32Error**   | AUCUNE \_ erreur                            |
| **Indicateurs**        | \_copie FILEOP                         |
| **Source**       | Chemin d’accès complet du fichier temporaire.     |
| **Cible**       | Chemin d’accès complet du fichier cible réel. |



 

Ce fichier temporaire sera copié dans le répertoire cible lors du redémarrage du système. Les fonctions de configuration génèrent automatiquement un chemin d’accès pour le fichier temporaire.

Si l’opération retardée est une opération de suppression de fichier, la structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) contient les informations suivantes.



| Membre FILEPATHS | Valeur                                |
|------------------|--------------------------------------|
| **Win32Error**   | AUCUNE \_ erreur                            |
| **Indicateurs**        | FILEOP \_ Supprimer                       |
| **Source**       | NULL                                 |
| **Cible**       | Chemin d’accès complet du fichier à supprimer. |



 

</dd> <dt>

*Param2* 
</dt> <dd>

N'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="requirements"></a>Configuration requise



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

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




