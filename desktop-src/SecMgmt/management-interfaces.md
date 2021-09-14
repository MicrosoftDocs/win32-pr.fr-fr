---
description: Répertorie les interfaces fournies par le moteur de pièce jointe.
ms.assetid: 451587bd-a7ab-446b-b647-be98de251915
title: Interfaces de gestion de la sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b3a205757a3bf324a5308a5f6fbc3d63374b4af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095826"
---
# <a name="security-management-interfaces"></a>Interfaces de gestion de la sécurité

Cette section contient des pages de référence pour les groupes d’interfaces suivants :

-   [Interfaces du moteur de pièce jointe](#attachment-engine-interfaces)

## <a name="attachment-engine-interfaces"></a>Interfaces du moteur de pièce jointe



| Interface                                                            | Description                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)               | Récupère les données de configuration et d’analyse relatives à un service de sécurité spécifié à partir des composants logiciels enfichables de configuration de sécurité. Les composants logiciels enfichables de configuration de la sécurité exposent cette interface, qui permet d’appeler les extensions de composant logiciel enfichable d’attachement pour demander des informations sur la configuration ou l’analyse.                                                 |
| [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) | Récupère les informations de configuration ou d’analyse modifiées à partir d’un composant logiciel enfichable pièce jointe. Les composants logiciels enfichables de configuration de la sécurité appellent cette interface pour récupérer toutes les informations modifiées à partir de l’extension du composant logiciel enfichable pièce jointe. Le composant logiciel enfichable Configuration de la sécurité stocke ensuite ces données de manière appropriée dans la base de données de sécurité. |



 

Pour plus d’informations sur les interfaces COM qui doivent être implémentées par les extensions de composant logiciel enfichable, consultez la documentation de la console MMC ( [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) ).

 

 
