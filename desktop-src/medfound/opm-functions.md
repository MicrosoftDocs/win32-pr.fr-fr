---
description: Les fonctions suivantes sont utilisées avec le gestionnaire de protection de sortie (OPM).
ms.assetid: 7ecde6ae-56fd-451b-bebb-224c6801be05
title: Fonctions OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de880584716c5caac94c93e48dd89ded481c14e1c7a08be3e23ac334e1c8bfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058763"
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

 

 



