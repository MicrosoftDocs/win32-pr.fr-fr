---
title: Interface ITsSbTargetEx
description: Expose les propriétés qui stockent les informations de configuration et d’état d’une cible.
ms.assetid: 3f0f26fb-e8bc-47eb-8038-e51792ad4376
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface ITsSbTargetEx
- Services Bureau à distance de l’interface ITsSbTargetEx, Description
topic_type:
- apiref
api_name:
- ITsSbTargetEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fb9be0e4cf5c0395efa93d308fdfa45362a7ac8919ab49a108700106aff6081b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989819"
---
# <a name="itssbtargetex-interface"></a>Interface ITsSbTargetEx

Expose les propriétés qui stockent les informations de configuration et d’état d’une cible.

cette interface est uniquement disponible sur Windows Server 2012 R2 avec [KB3091411](https://support.microsoft.com/kb/3091411) installé. La propriété [**TargetLoad**](itssbtarget-targetload.md) de l’interface [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) est disponible à partir de Windows Server 2016.

## <a name="members"></a>Membres

L’interface **ITsSbTargetEx** hérite de [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget). **ITsSbTargetEx** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **ITsSbTargetEx** possède les propriétés suivantes.



| Propriété                                                                      | Type d’accès           | Description                                                                               |
|:------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**EnvironmentName**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_environmentname)<br/>             | Lecture/écriture<br/> | Récupère ou spécifie le nom de l’environnement associé à la cible.<br/> |
| [**FarmName**](itssbtarget-farmname.md)<br/>                           | Lecture/écriture<br/> | Spécifie ou récupère le nom de la batterie de serveurs à laquelle cette cible est jointe.<br/>    |
| [**AdressesIP**](itssbtarget-ipaddresses.md)<br/>                     | Lecture/écriture<br/> | Récupère ou spécifie les adresses IP externes de la cible.<br/>                |
| [**NumPendingConnections**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numpendingconnections)<br/> | Lecture seule<br/>  | Récupère le nombre de connexions utilisateur en attente pour la cible.<br/>               |
| [**NumSessions**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numsessions)<br/>                     | Lecture seule<br/>  | Récupère le nombre de sessions gérées par le répartiteur pour la cible.<br/>          |
| [**TargetFQDN**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetfqdn)<br/>                       | Lecture/écriture<br/> | Spécifie ou récupère le nom de domaine complet de la cible.<br/>          |
| [**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))<br/>                     | Lecture seule<br/>  | Récupère le chargement relatif sur une cible.<br/>                                       |
| [**TargetName**](itssbtarget-targetname.md)<br/>                       | Lecture/écriture<br/> | Spécifie ou récupère le nom de la cible.<br/>                                 |
| [**TargetNetbios**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetnetbios)<br/>                 | Lecture/écriture<br/> | Spécifie ou récupère le nom NetBIOS de la cible.<br/>                         |
| [**TargetPropertySet**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetpropertyset)<br/>         | Lecture/écriture<br/> | Spécifie ou récupère le jeu de propriétés pour la cible.<br/>                        |
| [**TargetState**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate)<br/>                     | Lecture/écriture<br/> | Spécifie ou récupère l’État cible.<br/>                                       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2012 R2<br/>                                                |
| IID<br/>                      | IID \_ ITsSbTargetEx est défini en tant que 74f99987-625d-11e5-BEA1-a0481c7e9064<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[Bureau à distance les interfaces de virtualisation](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

