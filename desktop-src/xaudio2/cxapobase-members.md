---
description: Affiche les membres de la classe CXAPOBase.
ms.assetid: 0791888B-7215-475B-95C8-B558A1E57783
title: Membres CXAPOBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e76e1846b5dd9c28bec4f5cfe8e0168f5afbca012459b5860c4a5e23c610f6ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962738"
---
# <a name="cxapobase-members"></a>Membres CXAPOBase

Affiche les membres de la classe [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) .

## <a name="public-constructors"></a>Constructeurs publics



|                                |                                                     |
|--------------------------------|-----------------------------------------------------|
| [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) | Construit un objet [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) . |



 

## <a name="public-methods"></a>M&#233;thodes publiques



|                                                                                                                        |                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                   | Incrémente le décompte de références de l’objet XAPO.<br/>                                                                                                         |
| [**CalcInputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                     | Retourne le nombre de frames d’entrée requis pour générer le nombre donné de frames de sortie.<br/>                                                            |
| [**CalcOutputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Retourne le nombre de frames de sortie requis pour générer le nombre donné de frames d’entrée.<br/>                                                            |
| [**GetRegistrationProperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo)) | Retourne les propriétés d’inscription d’un XAPO.<br/>                                                                                                       |
| [**Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                               | Effectue une initialisation spécifique à l’effet.<br/>                                                                                                          |
| [**IsInputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))       | Interroge si un format d’entrée spécifique est pris en charge pour un format de sortie donné.<br/>                                                                            |
| [**IsOutputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))     | Interroge si un format de sortie spécifique est pris en charge pour un format d’entrée donné.<br/>                                                                            |
| [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                       | Notifie le XAPO de l' [**opération**](/windows/win32/api/xapo/nf-xapo-ixapo-process) de formatage de flux de données.<br/>                                                             |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Récupère le pointeur d’interface demandé si le XAPO le prend en charge.<br/>                                                                                    |
| [**Release**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                 | Décrémente le décompte de références de l’objet XAPO et supprime l’objet si le nombre de références est égal à zéro.<br/>                                             |
| [**Reset**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                         | Retourne l’objet à l’État dans lequel il se trouvait juste après l’appel de [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .<br/>                             |
| [**UnlockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Inverse de LockForProcess : les variables allouées pendant [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) doivent être désallouées dans cette méthode.<br/> |



 

## <a name="protected-methods"></a>Méthodes protégées



|                                                                                          |                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetRegistrationPropertiesInternal**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-getregistrationpropertiesinternal) | Retourne un pointeur vers la structure des [**\_ \_ propriétés d’inscription XAPO**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)contenant les propriétés d’inscription avec lesquelles le XAPO a été créé.<br/> |
| [**IsLocked**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-islocked)                                                   | Vérifie si le XAPO est verrouillé.<br/>                                                                                                                                                |
| LONG m \_ lReferenceCount<br/>                                                       | Nombre de références COM de l’objet XAPO.<br/>                                                                                                                                       |
| [**ProcessThru**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-processthru)                                             | Appelée par une implémentation de [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process) lorsqu’un XAPO est désactivé pour le traitement.<br/>                                                  |
| [**ValidateFormatDefault**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatdefault)                         | Vérifie qu’un format audio se trouve dans les plages par défaut prises en charge.<br/>                                                                                                     |
| [**ValidateFormatPair**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatpair)                               | Vérifie que la configuration d’une paire de formats d’entrée et de sortie est prise en charge par rapport aux indicateurs de propriété XAPO.<br/>                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CXAPOBase, classe**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)
</dt> </dl>

 

 
