---
description: Affiche les membres de la classe CXAPOParametersBase.
ms.assetid: C2113358-07DE-426E-AF26-BD8ED9902192
title: Membres CXAPOParametersBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e225d1628408b5d5472bed8c3060f714bb7b0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529291"
---
# <a name="cxapoparametersbase-members"></a>Membres CXAPOParametersBase

Affiche les membres de la classe [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) .

## <a name="public-constructors"></a>Constructeurs publics



|                                                    |                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) | Construit un objet [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) . |



 

## <a name="public-methods"></a>M&#233;thodes publiques



|                                                                                                                              |                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                         | Incrémente le décompte de références de l’objet XAPO.<br/>                                                                                                         |
| [**BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess)                                                                     | Retourne les paramètres de processus en cours. <br/>                                                                                                              |
| [**CalcInputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                           | Retourne le nombre de frames d’entrée requis pour générer le nombre donné de frames de sortie.<br/>                                                            |
| [**CalcOutputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Retourne le nombre de frames de sortie requis pour générer le nombre donné de frames d’entrée.<br/>                                                            |
| [**EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess)                                                                         | Notifie [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) que le XAPO a fini d’accéder aux paramètres du processus actuel. <br/>                     |
| [**GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters) (héritée de [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)) | Obtient les paramètres spécifiques à l’effet. <br/>                                                                                                                     |
| [**GetRegistrationProperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))       | Retourne les propriétés d’inscription d’un XAPO.<br/>                                                                                                       |
| [**Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                     | Effectue une initialisation spécifique à l’effet.<br/>                                                                                                          |
| [**IsInputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))             | Interroge si un format d’entrée spécifique est pris en charge pour un format de sortie donné.<br/>                                                                            |
| [**IsOutputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))           | Interroge si un format de sortie spécifique est pris en charge pour un format d’entrée donné.<br/>                                                                            |
| [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                             | Notifie le XAPO de l' [**opération**](/windows/win32/api/xapo/nf-xapo-ixapo-process) de formatage de flux de données.<br/>                                                             |
| [**OnSetParameters**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-onsetparameters)                                                               | Appelé par [**IXAPOParameters :: SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) pour permettre la validation des paramètres définis par l’utilisateur. <br/>          |
| [**ParametersChanged**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-parameterschanged)                                                           | Indique si [**IXAPOParameters :: SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) a été appelé depuis la dernière passe de traitement. <br/>       |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Récupère le pointeur d’interface demandé si le XAPO le prend en charge.<br/>                                                                                    |
| [**Release**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                       | Décrémente le décompte de références de l’objet XAPO et supprime l’objet si le nombre de références est égal à zéro.<br/>                                             |
| [**Reset**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                               | Retourne l’objet à l’État dans lequel il se trouvait juste après l’appel de [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .<br/>                             |
| [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) (héritée de [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)) | Définit des paramètres propres à l’effet.<br/>                                                                                                                      |
| [**UnlockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (héritée de [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Inverse de LockForProcess : les variables allouées pendant [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) doivent être désallouées dans cette méthode.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CXAPOParametersBase, classe**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)
</dt> </dl>

 

 
