---
description: Les valeurs définissent un type SAP spécifique.
ms.assetid: c0a1269b-f9d4-49e1-89ca-526fef148134
title: WLX_SAS_TYPE_XXX (Winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a75c7d7a71855700c4c8c233db3cfc18e06b9d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096161"
---
# <a name="wlx_sas_type_xxx"></a>\_type wlx \_ SAS \_ xxx

\[la constante WLX de \_ \_ TYPE SAS \_ XXX n’est plus disponible pour une utilisation à partir de Windows Server 2008 et Windows Vista.\]

Les valeurs de **\_ type SAS wlx \_ \_ xxx** définissent un type SAP spécifique.

> [!Note]  
> les dll GINA sont ignorées dans Windows Vista.

 

Toutes les valeurs comprises entre zéro et 127 sont réservées pour les types définis par Microsoft. Les valeurs supérieures à 127 sont disponibles pour les types définis par le client. Les types suivants sont passés aux fonctions qui ont un paramètre *dwSasType* .



| Constante                                                                                                                                                                                                         | Description                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_SAS_TYPE_CTRL_ALT_DEL"></span><span id="wlx_sas_type_ctrl_alt_del"></span><dl> <dt>**WLX \_ \_ type SAS \_ CTRL \_ Alt \_ Suppr**</dt> </dl>            | Indique qu’un utilisateur a tapé la combinaison de touches CTRL + ALT + SUPPR standard.<br/>                                                                                     |
| <span id="WLX_SAS_TYPE_SC_INSERT"></span><span id="wlx_sas_type_sc_insert"></span><dl> <dt>**WLX \_ de \_ type SAS \_ SC \_ Insert**</dt> </dl>                      | Indique qu’une [*carte à puce*](../secgloss/s-gly.md) a été insérée dans un appareil compatible.<br/> |
| <span id="WLX_SAS_TYPE_SC_REMOVE"></span><span id="wlx_sas_type_sc_remove"></span><dl> <dt>**\_type SAS \_ wlx \_ SC \_ Remove**</dt> </dl>                      | Indique qu’une carte à puce a été supprimée d’un appareil compatible.<br/>                                                                        |
| <span id="WLX_SAS_TYPE_SCRNSVR_ACTIVITY"></span><span id="wlx_sas_type_scrnsvr_activity"></span><dl> <dt>**\_ \_ activité SCRNSVR du type SAS \_ wlx \_**</dt> </dl> | Indique que l’activité du clavier ou de la souris s’est produite alors qu’un économiseur d’écran sécurisé était actif.<br/>                                                    |
| <span id="WLX_SAS_TYPE_SCRNSVR_TIMEOUT"></span><span id="wlx_sas_type_scrnsvr_timeout"></span><dl> <dt>**\_ \_ \_ \_ délai d’expiration du type SAS wlx SCRNSVR**</dt> </dl>    | Indique que l’activation de l’économiseur d’écran s’est produite en raison de l’inactivité du clavier et de la souris.<br/>                                                     |
| <span id="WLX_SAS_TYPE_TIMEOUT"></span><span id="wlx_sas_type_timeout"></span><dl> <dt>**\_ \_ \_ délai d’expiration du type SAS wlx**</dt> </dl>                             | Indique qu’aucune entrée utilisateur n’a été reçue dans le délai d’attente spécifié.<br/>                                                               |
| <span id="WLX_SAS_TYPE_USER_LOGOFF"></span><span id="wlx_sas_type_user_logoff"></span><dl> <dt>**\_déconnexion \_ utilisateur du type SAS \_ wlx \_**</dt> </dl>                | Indique que l’utilisateur est déconnecté du système.<br/>                                                                                            |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                               |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winwlx. h</dt> </dl> |



 

 
