---
title: Clés de Registre WCS
description: WCS utilise des clés de Registre pour signaler que certains événements de profil de couleurs se sont produits. Les applications doivent interroger ces clés de Registre pour mettre à jour l’état du profil de couleurs système.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Windows Color System (WCS), clés de Registre
- WCS (Windows Color System), clés de Registre
- gestion des couleurs des images, clés de Registre
- gestion des couleurs, clés de Registre
- couleurs, clés de Registre
- Référence WCS, clés de Registre
- référence pour WCS, clés de Registre
- Système de couleurs Windows (WCS), registre
- WCS (système de couleurs Windows), registre
- gestion des couleurs des images, registre
- gestion des couleurs, registre
- couleurs, registre
- Référence WCS, registre
- référence pour WCS, registre
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a1c0072d9a00fe0cff4a4dbe57af839f65731b
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "106538418"
---
# <a name="wcs-registry-keys"></a>Clés de Registre WCS

WCS utilise des clés de Registre pour signaler que certains événements de profil de couleurs se sont produits. Les applications doivent interroger ces clés de Registre pour mettre à jour l’état du profil de couleurs système.

## <a name="active-color-profile-changed"></a>Profil de couleurs actif modifié

Les applications peuvent souhaiter répondre aux événements de modification du profil de couleurs pour un appareil moniteur ; Cela garantit qu’ils disposent toujours d’informations de couleur précises pour leur cible, même si l’utilisateur ou une autre application a modifié le profil actif de l’appareil.

### <a name="desktop-applications"></a>Applications de bureau

Les applications de bureau doivent écouter les modifications apportées au registre pour déterminer quand des associations de profil de couleurs ont été modifiées à l’aide de [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue). Une application doit s’inscrire à la fois pour les modifications d’association de profil par utilisateur et pour les modifications à l’ensemble du système.

[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) doit être initialisé avec un HKEY fourni par [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa). **RegOpenKeyEx** doit être initialisé à l’aide des emplacements de l’arborescence du registre suivants :



|                                  |                                                                                                                                                    |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Associations de profils par utilisateur    | **HKEY \_ Current \_ User Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ICM \\ ProfileAssociations \\ Display \\ {4d36e96e-E325-11CE-BFC1-08002BE10318}** |
| Associations de profils à l’ensemble du système | **HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ Class \\ {4d36e96e-E325-11CE-BFC1-08002BE10318}**                                        |



 

Lorsque l’application est avertie d’une modification de clé de Registre, elle doit d’abord demander si des associations par utilisateur ou au niveau du système sont utilisées en appelant [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent). Elle doit ensuite appeler [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) avec la valeur de l' [**\_ étendue de \_ gestion \_ du profil WCS**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) approprié pour obtenir le nouveau profil de couleurs actif pour l’analyse. Notez que toutes les modifications apportées à la clé de registre ne correspondent pas à une modification réelle du profil de couleurs actuellement actif ; l’application doit vérifie si le profil retourné par **WcsGetDefaultColorProfile** a réellement changé.

### <a name="universal-windows-uwp-apps"></a>Applications Windows universelles (UWP)

Les applications Windows universelles n’ont pas accès aux clés de Registre ci-dessus. Au lieu de cela, ils doivent inscrire un gestionnaire pour l’événement [**DisplayInformation. ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) . Cet événement se déclenche chaque fois que le profil de couleurs actif du moniteur sur lequel l’application s’exécute a changé. ColorProfileChanged prend en compte si les associations de profils par utilisateur ou au niveau du système sont utilisées ; ces informations sont extraites des applications UWP.

Lors de la réponse à l’événement ColorProfileChanged, l’application doit interroger le profil actuellement actif à l’aide de [**DisplayInformation. GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).

 

 