---
title: Nouveautés de Windows Vista
description: La version 1,0 de la gestion des couleurs des images (ICM) a été fournie dans Microsoft Windows 95 et fournit des fonctionnalités de gestion des couleurs de base dans les contextes de périphérique Windows.
ms.assetid: 3079f84c-0d6c-4f87-a041-de86f5f7d99b
keywords:
- Windows Color System (WCS), Windows Vista
- WCS (Windows Color System), Windows Vista
- gestion des couleurs des images, Windows Vista
- gestion des couleurs, Windows Vista
- couleurs, Windows Vista
- Windows Color System (WCS), systèmes d’exploitation
- WCS (système de couleurs Windows), systèmes d’exploitation
- gestion des couleurs des images, systèmes d’exploitation
- gestion des couleurs, systèmes d’exploitation
- couleurs, systèmes d’exploitation
- ICM (Image Color Management)
- ICM (gestion des couleurs d’image)
- Gestion des couleurs de Windows Vista
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b889dd0ba3b044f0d0f158bd2364f5c3216ec39
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "106525775"
---
# <a name="whats-new-in-windows-vista"></a>Nouveautés de Windows Vista

La version 1,0 de la gestion des couleurs des images (ICM) a été fournie dans Microsoft Windows 95 et fournit des fonctionnalités de gestion des couleurs de base dans les contextes de périphérique Windows.

ICM version 2,0 a été fourni dans Windows 98, Windows Millennium Edition, Windows 2000 et WindowsXP. il comprenait une variété de nouvelles fonctions qui implémentaient la gestion des couleurs en dehors des contextes de périphérique. Ces nouvelles fonctions étaient appropriées pour des exigences de gestion des couleurs plus exigeantes et permettaient aux applications de mieux contrôler le processus de gestion des couleurs.

Avec la sortie de Windows Vista, ICM 2,0 est désormais inclus dans Windows Color System (WCS) 1,0, qui offre davantage de fonctionnalités. Le tableau suivant répertorie les nouvelles interfaces de programmation d’applications (API) fournies dans Windows Vista.

## <a name="new-api-shipping-in-windows-vista"></a>Nouvelle API d’expédition dans Windows Vista



Énumérations

Nom de l’API

En-tête

Bibliothèque

[**COLORDATATYPE**](/windows/win32/api/icm/ne-icm-colordatatype)

ICM. h

MSCMS. lib

[**COLORPROFILESUBTYPE**](/windows/win32/api/icm/ne-icm-colorprofilesubtype)

ICM. h

MSCMS. lib

[**COLORPROFILETYPE**](/windows/win32/api/icm/ne-icm-colorprofiletype)

ICM. h

MSCMS. lib

[**\_étendue de \_ gestion des profils WCS \_**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)

ICM. h

MSCMS. lib



 



Fonctions

Nom de l’API

En-tête

Bibliothèque

[**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

ICM. h

MSCMS. lib

[**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

ICM. h

MSCMS. lib

[**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)

ICM. h

MSCMS. lib

[**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice)

ICM. h

MSCMS. lib

[**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)

ICM. h

MSCMS. lib

[**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)

ICM. h

MSCMS. lib

[**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)

ICM. h

MSCMS. lib

[**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize)

ICM. h

MSCMS. lib

[**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

ICM. h

MSCMS. lib

[**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

ICM. h

MSCMS. lib

[**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew)

ICM. h

MSCMS. lib

[**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile)

ICM. h

MSCMS. lib

[**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent)

ICM. h

MSCMS. lib

[**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)

ICM. h

MSCMS. lib

[**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors)

ICM. h

MSCMS. lib



 



Interfaces et leurs fonctions

Nom de l’API

En-tête

Bibliothèque

[**IDeviceModelPlugin**](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)

WcsPlugIn. h

N/A

[**IDeviceModelPlugin::ColorimetricToDeviceColors**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolors)

WcsPlugIn. h

N/A

[**IDeviceModelPlugin::ColorimetricToDeviceColorsWithBlack**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack)

WcsPlugIn. h

N/A

[**IDeviceModelPlugin ::D eviceToColorimetricColors**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-devicetocolorimetriccolors)

WcsPlugIn. h

N/A

[**IDeviceModelPlugin::GetGamutBoundaryMesh**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymesh)

WcsPlugIn. h

N/A

[**IDeviceModelPlugin::GetGamutBoundaryMeshSize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymeshsize)

WcsPlugIn. h

N/A

[**IDeviceModelPlugin::GetNeutralAxis**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxis)

WcsPlugIn. h

N/A

[**IDeviceModelPlugin::GetNeutralAxisSize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxissize)

WcsPlugIn. h

N/A

[**IDeviceModelPlugin::GetNumChannels**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getnumchannels)

WcsPlugIn. h

N/A

[**IDeviceModelPlugin::GetPrimarySamples**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getprimarysamples)

WcsPlugIn. h

N/A

[**IDeviceModelPlugin :: Initialize**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-initialize)

WcsPlugIn. h

N/A

[**IDeviceModelPlugin::SetTransformDeviceModelInfo**](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-settransformdevicemodelinfo)

WcsPlugIn. h

N/A

[**IGamutMapModelPlugin**](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-igamutmapmodelplugin)

WcsPlugIn. h

N/A

[**IGamutMapModelPlugin :: Initialize**](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-initialize)

WcsPlugIn. h

N/A

[**IGamutMapModelPlugin::SourceToDestinationAppearanceColors**](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-sourcetodestinationappearancecolors)

WcsPlugIn. h

N/A



 



Structures

Nom de l’API

En-tête

Bibliothèque

[**BlackInformation**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation)

WcsPlugIn. h

N/A

[**GamutBoundaryDescription**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutboundarydescription)

WcsPlugIn. h

N/A

[**XYZColorF**](https://www.bing.com/search?q=**XYZColorF**)

WcsPlugIn. h

N/A

[**JChColorF**](https://www.bing.com/search?q=**JChColorF**)

WcsPlugIn. h

N/A

[**JabColorF**](https://www.bing.com/search?q=**JabColorF**)

WcsPlugIn. h

N/A

[**GamutShell**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshell)

WcsPlugIn. h

N/A

[**GamutShellTriangle**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshelltriangle)

WcsPlugIn. h

N/A

[**PrimaryJabColors**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryjabcolors)

WcsPlugIn. h

N/A

[**PrimaryXYZColors**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryxyzcolors)

WcsPlugIn. h

N/A



 

 

 