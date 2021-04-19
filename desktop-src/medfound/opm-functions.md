---
description: Les fonctions suivantes sont utilisées avec le gestionnaire de protection de sortie (OPM).
ms.assetid: 7ecde6ae-56fd-451b-bebb-224c6801be05
title: Fonctions OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b4ef210ace3f7f179b59980cedb962a5bee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520429"
---
# <a name="opm-functions"></a>Fonctions OPM

Les fonctions suivantes sont utilisées avec le [Gestionnaire de protection de sortie](output-protection-manager.md) (OPM).



| Fonction                                                                                             | Description                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**OPMGetVideoOutputForTarget**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputfortarget)                                     | Retourne un objet de sortie vidéo pour la cible VidPN sur l’adaptateur spécifié.                                                          |
| [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)                             | Crée un objet de sortie Protection Manager (OPM) pour chaque moniteur physique associé à un handle **HMONITOR** particulier. |
| [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) | Crée un objet OPM pour chaque moniteur physique associé à un appareil Direct3D particulier.                                 |



 

Les fonctions suivantes sont utilisées par OPM pour accéder aux fonctionnalités dans le pilote d’affichage. Les applications ne doivent pas appeler ces fonctions.

-   [**ConfigureOPMProtectedOutput**](configureopmprotectedoutput.md)
-   [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)
-   [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md)
-   [**GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate)
-   [**GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize)
-   [**GetCOPPCompatibleOPMInformation**](getcoppcompatibleopminformation.md)
-   [**GetOPMInformation**](getopminformation.md)
-   [**GetOPMRandomNumber**](getopmrandomnumber.md)
-   [**GetSuggestedOPMProtectedOutputArraySize**](getsuggestedopmprotectedoutputarraysize.md)
-   [**SetOPMSigningKeyAndSequenceNumbers**](setopmsigningkeyandsequencenumbers.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur la programmation OPM](opm-programming-reference.md)
</dt> <dt>

[Gestionnaire de protection de sortie](output-protection-manager.md)
</dt> </dl>

 

 



