---
title: Gestion des événements d’individualisation
description: Gestion des événements d’individualisation
ms.assetid: f533978f-f366-4900-b784-f51e88393984
keywords:
- Windows Media Format SDK, gestion des événements d’individualisation
- Windows Media Format SDK, événements d’individualisation
- ASF (Advanced Systems Format), gestion des événements d’individualisation
- ASF (format de systèmes avancés), gestion des événements d’individualisation
- ASF (Advanced Systems Format), événements de individualisation
- ASF (format des systèmes avancés), événements d’individualisation
- gestion des droits numériques (DRM), gestion des événements d’individualisation
- DRM (gestion des droits numériques), gestion des événements d’individualisation
- gestion des droits numériques (DRM), événements d’individualisation
- DRM (gestion des droits numériques), événements d’individualisation
- événements d’individualisation
- événements, événements d’individualisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 895710558c58fca108915ad1a73a0354c1fb39feb662fa3e2c698dadbe4cbe76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433614"
---
# <a name="handling-individualization-events"></a>Gestion des événements d’individualisation

Lorsqu’une application DRM tente d’ouvrir un fichier protégé, le composant DRM examine l’attribut [**\_ \_ IndividualizedVersion DRM DRMHeader**](drm-drmheader-individualizedversion.md) dans le fichier, qui spécifie le niveau de version minimal requis pour accéder au contenu. tous les niveaux du composant DRM fonctionnent avec toutes les versions 7,0 et ultérieures de Lecteur Windows Media et le kit de développement logiciel (SDK) Windows Media Format. Si le niveau de version individualisé du composant DRM est inférieur à la version requise, le composant DRM enverra un événement **d' \_ \_ individualisation** à la méthode [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) de l’application. L’application doit ensuite afficher un message ou une boîte de dialogue invitant les utilisateurs à démarrer ou à annuler la mise à niveau de sécurité. Cette invite est nécessaire car, pour des raisons de confidentialité, les utilisateurs doivent donner leur autorisation avant l’installation d’une mise à niveau de sécurité sur leur ordinateur.

> [!Note]  
> L’en-tête du contenu spécifie uniquement les deux premiers chiffres pour DRM \_ DRMVersion \_ IndividualizedVersion. En d’autres termes, pour exiger un composant DRM de niveau 2.2.0.1, l’en-tête contient « 2,2 ».

 

Pour démarrer la mise à niveau de sécurité et/ou déclencher l’individualisation, appelez la méthode [**IWMDRMReader :: Individual**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) avec le paramètre *dwFlags* défini sur 1.

Vous devez gérer l' **événement \_ Individual WMT** dans votre application. Cet événement est déclenché plusieurs fois par le composant DRM avec l’état du processus d’individualisation indiqué dans le paramètre *pValue* , qui est converti en pointeur vers une structure d' [**État de l' \_ individualisation \_ WM**](wm-individualize-status.md) .

Une fois le composant DRM correctement individualisé, l’application reçoit un événement **WMT \_ no \_ Rights \_ ex** , qui indique que l’application peut maintenant continuer à acquérir une licence pour le contenu.

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gestion des événements d’acquisition de licence**](handling-license-acquisition-events.md)
</dt> <dt>

[**Individualiser des applications DRM**](individualizing-drm-applications.md)
</dt> <dt>

[**Interface IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> </dl>

 

 




