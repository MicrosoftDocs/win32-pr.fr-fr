---
description: Commandes OPM
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: Commandes OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b00240925c28322b911ab55a0e4f026f051d6ec
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119144"
---
# <a name="opm-commands"></a>Commandes OPM

Cette section répertorie les commandes disponibles pour le [Gestionnaire de protection de sortie](output-protection-manager.md) (OPM).

Pour envoyer une commande OPM, appelez [**IOPMVideoOutput :: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure). Pour chaque commande, les informations suivantes sont affichées.



| Value             | Description                                                                                                                                                            |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de la commande | Identifie la commande. Définissez la valeur du membre **guidSetting** de la structure des [**\_ \_ paramètres de configuration OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) comme égale à cette valeur. |
| Données d’entrée   | Spécifie comment interpréter le tableau **abParameters** dans la structure des [**\_ \_ paramètres de configuration de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) .                      |



 

Les commandes suivantes sont définies :



| Commande                                                                                                       | Description                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**\_ \_ \_ signaux ACP et \_ CGMSA de \_ l’ensemble OPM**](opm-set-acp-and-cgmsa-signaling.md)                               | Spécifie des informations sur le signal vidéo, autres que le niveau de protection.                      |
| [**\_SRM Set \_ HDCP \_**](opm-set-hdcp-srm.md)                                                               | Met à jour le message de renouvellement du système (SRM) pour High-Bandwidth protection du contenu numérique (HDCP). |
| [**niveau de protection de l' \_ ensemble OPM \_ \_**](opm-set-protection-level.md)                                               | Définit le niveau de protection d’un mécanisme de protection de sortie.                                       |
| [**\_ \_ niveau de protection de l’ensemble OPM \_ selon le \_ \_ \_ \_ DVD CSS**](opm-set-protection-level-according-to-css-dvd.md) | Définit le niveau de protection HDCP pour la lecture des DVD, en suivant les règles du système de brouillage du contenu DVD (CSS). |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur la programmation OPM](opm-programming-reference.md)
</dt> <dt>

[Gestionnaire de protection de sortie](output-protection-manager.md)
</dt> </dl>

 

 



