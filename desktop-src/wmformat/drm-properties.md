---
title: Propriétés DRM
description: Propriétés DRM
ms.assetid: 862fc8bc-6e40-4496-862a-c12c8a382116
keywords:
- Windows Media Format SDK, propriétés DRM
- ASF (Advanced Systems Format), propriétés DRM
- ASF (format des systèmes avancés), propriétés DRM
- gestion des droits numériques (DRM), propriétés
- DRM (gestion des droits numériques), propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb8542d360c38ab3f12406462cefc0454e7eae33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029872"
---
# <a name="drm-properties"></a>Propriétés DRM

Le tableau suivant répertorie les propriétés DRM que les applications peuvent recevoir ou définir lors de l’écriture ou de la lecture de fichiers protégés. Ces propriétés ne sont pas des attributs de fichier ; ils ne sont pas écrits dans l’en-tête de fichier ASF.



| Propriété DRM                                                                             | Identificateur global                               | Type de données             |
|------------------------------------------------------------------------------------------|-------------------------------------------------|-----------------------|
| [**\_ACTIONALLOWED DRM**](drm-actionallowed.md)                                          | g \_ wszWMDRM \_ ActionAllowed                      | **\_type WMT \_ bool**   |
| [**\_Sauvegarde ACTIONALLOWED \_ DRM**](drm-actionallowed-backup.md)                           | c \_ wszWMDRM \_ ActionAllowed \_ sauvegarde              | **\_type WMT \_ bool**   |
| [**\_ACTIONALLOWED DRM \_ CollaborativePlay**](drm-actionallowed-collaborativeplay.md)     | g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay   | **\_type WMT \_ bool**   |
| [**\_Copie DRM ActionAllowed \_**](drm-actionallowed-copy.md)                               | \_wszWMDRM g \_ ActionAllowed \_ copie                | **\_type WMT \_ bool**   |
| [**\_ACTIONALLOWED DRM \_ CopyToCD**](drm-actionallowed-copytocd.md)                       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD            | **\_type WMT \_ bool**   |
| [**\_ACTIONALLOWED DRM \_ CopyToNonSDMIDevice**](drm-actionallowed-copytononsdmidevice.md) | g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice | **\_type WMT \_ bool**   |
| [**\_ACTIONALLOWED DRM \_ CopyToSDMIDevice**](drm-actionallowed-copytosdmidevice.md)       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice    | **\_type WMT \_ bool**   |
| [**\_Lecture DRM ActionAllowed \_**](drm-actionallowed-playback.md)                       | \_lecture wszWMDRM \_ ActionAllowed \_ g            | **\_type WMT \_ bool**   |
| [**\_ACTIONALLOWED DRM \_ PlaylistBurn**](drm-actionallowed-playlistburn.md)               | g \_ wszWMDRM \_ ActionAllowed \_ PlaylistBurn        | **\_type WMT \_ bool**   |
| [**\_BASELICENSEACQURL DRM**](drm-baselicenseacqurl.md)                                  | g \_ wszWMDRM \_ BaseLicenseAcqURL                  | **\_chaîne de type WMT \_** |
| [**\_Indicateurs DRM**](drm-flags.md)                                                          | \_indicateurs wszWMDRM \_ g                              | **\_valeur DWORD de type WMT \_**  |
| [**\_HEADERSIGNPRIVKEY DRM**](drm-headersignprivkey.md)                                  | g \_ wszWMDRM \_ HeaderSignPrivKey                  | **\_chaîne de type WMT \_** |
| [**\_ISDRM DRM**](drm-isdrm.md)                                                          | \_wszIsDRM g                                     | **\_type WMT \_ bool**   |
| [**\_ISDRMCACHED DRM**](drm-isdrmcached.md)                                              | \_wszIsDRMCached g                               | **\_type WMT \_ bool**   |
| [**Keyseed DRM \_**](drm-keyseed.md)                                                      | g \_ wszWMDRM \_ keyseed                            | **\_chaîne de type WMT \_** |
| [**\_Niveau DRM**](drm-level.md)                                                          | \_niveau de wszWMDRM g \_                              | **\_valeur DWORD de type WMT \_**  |
| [**\_LICENSEID DRM**](drm-licenseid.md)                                                  | g \_ wszWMDRM \_ LicenseID                          | **\_chaîne de type WMT \_** |
| [**\_LICENSESTATE DRM**](drm-licensestate.md)                                            | g \_ wszWMDRM \_ LicenseState                       | **\_valeur DWORD de type WMT \_**  |
| [**\_LICENSESTATE DRM \_ CollaborativePlay**](drm-licensestate-collaborativeplay.md)       | g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay    | **\_binaire de type WMT \_** |
| [**\_Copie DRM LicenseState \_**](drm-licensestate-copy.md)                                 | \_wszWMDRM g \_ LicenseState \_ copie                 | **\_binaire de type WMT \_** |
| [**\_LICENSESTATE DRM \_ CopyToCD**](drm-licensestate-copytocd.md)                         | g \_ wszWMDRM \_ LicenseState \_ CopyToCD             | **\_binaire de type WMT \_** |
| [**\_LICENSESTATE DRM \_ CopyToSDMIDevice**](drm-licensestate-copytosdmidevice.md)         | g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice     | **\_binaire de type WMT \_** |
| [**\_LICENSESTATE DRM \_ CopyToNonSDMIDevice**](drm-licensestate-copytononsdmidevice.md)   | g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice  | **\_binaire de type WMT \_** |
| [**\_Lecture DRM LicenseState \_**](drm-licensestate-playback.md)                         | \_lecture wszWMDRM \_ LicenseState \_ g             | **\_binaire de type WMT \_** |
| [**\_LICENSESTATE DRM \_ PlaylistBurn**](drm-licensestate-playlistburn.md)                 | g \_ wszWMDRM \_ LicenseState \_ PlaylistBurn         | **\_binaire de type WMT \_** |
| [**\_Droits DRM**](drm-rights.md)                                                        | \_droits wszWMDRM \_ g                             | **\_chaîne de type WMT \_** |
| [**\_SAPLEVEL DRM**](drm-saplevel--deprecated.md)                                        | g \_ wszWMDRM \_ SAPLEVEL                           | **\_chaîne de type WMT \_** |
| [**Utiliser \_ \_ DRM avancé**](use-advanced-drm.md)                                           | g \_ wszWMUse \_ - \_ DRM avancé                      | **\_type WMT \_ bool**   |
| [**Utiliser \_ DRM**](use-drm.md)                                                              | g \_ wszWMUse \_ DRM                                | **\_type WMT \_ bool**   |
| [**Révocation WMDRMNET \_**](wmdrmnet-revocation.md)                                      | révocation de \_ wszWMDRMNET g \_                      | **\_chaîne de type WMT \_** |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Liste des attributs DRM**](drm-attribute-list.md)
</dt> </dl>

 

 




