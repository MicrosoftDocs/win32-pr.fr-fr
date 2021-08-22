---
title: Liste alphabétique de toutes les fonctions WCS
description: voici une liste alphabétique complète des fonctions de l’API WCS 1,0 fournies par Windows \ 160 ; 98 et versions ultérieures et Windows \ 160 ; 2000 et versions ultérieures.
ms.assetid: aba45dbd-6fc2-4788-87f0-043579fa53f9
keywords:
- Windows Système de couleurs (WCS), fonctions
- WCS (Windows Color System), fonctions
- gestion des couleurs des images, fonctions
- gestion des couleurs, fonctions
- couleurs, fonctions
- Référence WCS, fonctions
- référence pour WCS, functions
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e2c9250cc9fb1e9e418079ed3b9524b3add2535dd780eed65ae998bda80ef5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706659"
---
# <a name="alphabetical-list-of-all-wcs-functions"></a>Liste alphabétique de toutes les fonctions WCS

voici une liste alphabétique complète des fonctions de l’API WCS 1,0 fournies par Windows 98 et versions ultérieures et Windows 2000 et versions ultérieures.



| Fonction ou structure                                                                 | Description                                                                                                                                          |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (ou **ApplyCallbackFunction**) est une fonction de rappel que vous implémentez pour mettre à jour les données de configuration WCS pendant que la boîte de dialogue affichée par la fonction [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) s’exécute. |
| [**AssociateColorProfileWithDeviceW**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | Associe un profil de couleurs spécifié à un périphérique spécifié.                                                                                                            |
| [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Vérifie si les pixels d’une bitmap spécifiée se trouvent dans la [gamme](g.md) de sortie d’une transformation spécifiée. |
| [**CheckColors**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Détermine si les couleurs d’un tableau se trouvent dans la [gamme](g.md) de sortie d’une transformation spécifiée. |
| [**CheckColorsInGamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                                       | Vérifie si les couleurs spécifiées se trouvent dans la gamme d’appareils.                                                                                                      |
| [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | Ferme un handle de profil ouvert. |
| [**CMCheckColors**](/windows/win32/api/icm/nf-icm-cmcheckcolors) | Détermine si les couleurs spécifiées se trouvent dans la [gamme](./g.md) de sortie d’une transformation spécifiée. |
| [**CMCheckColorsInGamut**](/windows/win32/api/icm/nf-icm-cmcheckcolorsingamut) | Détermine si les triplets RGB spécifiés se trouvent dans la [gamme](./g.md) de sortie d’une transformation spécifiée. |
| [**CMCheckRGBs**](/windows/desktop/api/Wingdi/)                                                     | Vérifie les couleurs de bitmap par rapport à une gamme de sortie.                                                                                                        |
| [**CMConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-cmconvertcolornametoindex) | Convertit les noms de couleurs dans un espace de couleurs nommé en nombres indexés dans un profil de couleurs |
| [**CMConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-cmconvertindextocolorname) | Transforme des index dans un espace de couleurs en un tableau de noms dans un espace de couleurs nommé. |
| [**CMCreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-cmcreatedevicelinkprofile) | Crée un [profil de lien de périphérique](./d.md) dans le format spécifié par le consortium de couleurs international dans sa spécification de format de profil ICC. |
| [**CMCreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-cmcreatemultiprofiletransform) | Accepte un tableau de profils ou un [profil de lien d’appareil](./d.md) unique et crée une transformation de couleur. Cette transformation est un mappage de l’espace colorimétrique spécifié par le premier profil à celui du deuxième profil, et ainsi de suite jusqu’au dernier. |
| [**CMCreateProfile**](/windows/win32/api/icm/nf-icm-cmcreateprofile) | Crée un profil de couleurs d’affichage à partir d’une structure [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) . |
| [**CMCreateProfileW**](/windows/win32/api/icm/nf-icm-cmcreateprofilew) | Crée un profil de couleurs d’affichage à partir d’une structure [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) . |
| [**CMCreateTransform**](/windows/win32/api/icm/nf-icm-cmcreatetransform) | Action déconseillée. Il n’existe aucune API de remplacement, car celle-ci n’a plus été utilisée. Les développeurs d’autres modules CMM n’ont pas besoin de l’implémenter. |
| [**CMCreateTransformExt**](/windows/win32/api/icm/nf-icm-cmcreatetransformext) | Crée une transformation de couleur qui mappe un [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) d’entrée à un espace cible facultatif, puis à un périphérique de sortie, à l’aide d’un jeu d’indicateurs qui définissent la façon dont la transformation doit être créée. |
| [**CMCreateTransformExtW**](/windows/win32/api/icm/nf-icm-cmcreatetransformextw) | Crée une transformation de couleur qui mappe un [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) d’entrée à un espace cible facultatif, puis à un périphérique de sortie, à l’aide d’un jeu d’indicateurs qui définissent la façon dont la transformation doit être créée. |
| [**CMCreateTransformW**](/windows/win32/api/icm/nf-icm-cmcreatetransformw) | Action déconseillée. Il n’existe aucune API de remplacement, car celle-ci n’a plus été utilisée. Les développeurs d’autres modules CMM n’ont pas besoin de l’implémenter. |
| [**CMDeleteTransform**](/windows/win32/api/icm/nf-icm-cmdeletetransform) | Supprime une transformation de couleur spécifiée et libère toute mémoire qui lui est associée. |
| [**CMGetInfo**](/windows/win32/api/icm/nf-icm-cmgetinfo) | Récupère diverses informations sur le module de gestion des couleurs (CMM). |
| [**CMGetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-cmgetnamedprofileinfo) | Récupère des informations sur le profil de couleurs nommé spécifié. |
| [**CMGetPS2ColorRenderingDictionary**](/windows/desktop/api/Wingdi/)           | obtient un dictionnaire de rendu de couleurs PostScript.                                                                                                        |
| [**CMGetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-cmgetps2colorrenderingintent) | récupère l' [intention de rendu](rendering-intents.md) de couleur de niveau 2 PostScript à partir d’un profil. |
| [**CMGetPS2ColorSpaceArray**](/windows/desktop/api/Wingdi/)                             | obtient un tableau d’espace de couleurs PostScript.                                                                                                                 |
| [**CMIsProfileValid**](/windows/win32/api/icm/nf-icm-cmisprofilevalid) | Indique si le profil donné est un profil ICC valide qui peut être utilisé pour la gestion des couleurs. |
| [**CMTranslateColors**](/windows/win32/api/icm/nf-icm-cmtranslatecolors) | Convertit un tableau de couleurs d’un [espace de couleurs](color-spaces.md) source en un espace de couleurs de destination à l’aide d’une transformation de couleur. |
| [**CMTranslateRGB**](/windows/win32/api/icm/nf-icm-cmtranslatergb) | Traduit un RGBQuad fourni par l’application dans l’espace de [couleurs](color-spaces.md)du périphérique. |
| [**CMTranslateRGBs**](/windows/win32/api/icm/nf-icm-cmtranslatergbs) | Convertit une bitmap d’un [espace de couleurs](color-spaces.md) à un autre à l’aide d’une transformation de couleur. |
| [**CMTranslateRGBsExt**](/windows/win32/api/icm/nf-icm-cmtranslatergbsext) | Convertit une bitmap d’un format défini dans un format défini différent et appelle une fonction de rappel régulièrement, si elle est spécifiée, pour signaler la progression et permettre à l’application appelante de mettre fin à la traduction. |
| [**ColorCorrectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                                     | Corrige les entrées dans une palette pour un contexte de périphérique.                                                                                              |
| [**ColorMatchToTarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                                       | Effectue un mappage des couleurs à des fins de préversion.                                                                                                         |
| [**ConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | Convertit les noms de couleurs dans un espace de couleurs nommé en nombres d’index dans un profil de couleurs ICC (International Color Consortium). |
| [**ConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | Transforme des index dans un espace de couleurs en un tableau de noms dans un espace de couleurs nommé. |
| [**CreateColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                                           | Crée un espace de couleurs.                                                                                                                               |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransforma) | Transforme des index dans un espace de couleurs en un tableau de noms dans un espace de couleurs nommé. |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) | Transforme des index dans un espace de couleurs en un tableau de noms dans un espace de couleurs nommé. |
| [**CreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | Accepte un tableau de profils ou un [profil de lien d’appareil](d.md) unique et crée une transformation de couleur que les applications peuvent utiliser pour effectuer le mappage des couleurs. |
| [**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew) | Convertit un [espace de couleurs](c.md) logique en un [profil de périphérique](d.md). |
| [**DeleteColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                                           | Supprime un espace de couleurs.                                                                                                                               |
| [**DeleteColorTransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | Supprime une transformation de couleur donnée. |
| [**DisassociateColorProfileFromDeviceW**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | Dissocie un profil de couleurs spécifié avec un périphérique spécifié sur un ordinateur spécifié. |
| [**EnumColorProfilesW**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | Énumère tous les profils qui remplissent les critères d’énumération donnés. |
| [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                                             | Énumère les profils de couleur de sortie disponibles pour un contexte de périphérique donné.                                                                               |
| [**EnumICMProfilesProcCallback**](/windows/desktop/api/Wingdi/)                     | Fonction de rappel définie par l’application pour [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).                                                                |
| [**GetCMMInfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | Récupère diverses informations sur le module de gestion des couleurs (CMM) qui a créé la transformation de couleur spécifiée. |
| [**GetColorDirectoryW**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | récupère le chemin d’accès du répertoire de couleurs Windows sur un ordinateur spécifié. |
| [**GetColorProfileElement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | Copie les données d’un élément de profil balisé spécifié d’un profil de couleurs spécifié dans une mémoire tampon. |
| [**GetColorProfileElementTag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | Récupère le nom de balise spécifié par *dwIndex* dans la table des balises d’un profil de couleurs ICC (International Color Consortium) donné, où *dwIndex* est un index de base 1 dans cette table. |
| [**GetColorProfileFromHandle**](/windows/win32/api/icm/getcolorprofilefromhandle)                         | Récupère le contenu du profil de couleurs en fonction d’un handle d’un profil de couleurs ouvert.                                                                        |
| [**GetColorProfileHeader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | Récupère ou dérive une structure d’en-tête ICC à partir du profil de couleurs ICC ou du profil XML WCS. Les pilotes et les applications doivent supposer que retourne la **valeur true** indique qu’un en-tête correctement structuré est retourné. Chaque balise doit toujours être validée indépendamment à l’aide de l’API ICM2 héritée ou des API de schéma XML. |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | Obtient l’espace colorimétrique d’entrée actuel dans un contexte de périphérique. |
| [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | Récupère le nombre d’éléments avec balises dans un profil de couleurs donné. |
| [**GetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | Obtient la rampe gamma à partir des panneaux d’affichage de couleur directe.                                                                                                |
| [**GetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                                                 | Obtient le profil de couleur de sortie actuel d’un contexte de périphérique.                                                                                           |
| [**GetLogColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                                           | Obtient la structure [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) d’un contexte de périphérique.                                                                       |
| [**GetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | Récupère des informations sur le profil de couleurs nommé ICC (International Color Consortium) qui est spécifié dans le premier paramètre. |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | récupère le dictionnaire de rendu de couleur de PostScript niveau 2 à partir du profil de couleurs ICC spécifié. |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | récupère l' [intention de rendu](r.md) de couleur de niveau 2 PostScript à partir d’un profil de couleurs ICC. |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | récupère le PostScript tableau d' [espace de couleurs](c.md) de niveau 2 à partir d’un profil de couleurs ICC. |
| [**GetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | Récupère le profil de couleurs inscrit pour l’espace de [couleurs](c.md)standard spécifié. |
| [**ICMProgressProcCallback**](icmprogressproccallback.md)                             | Rappel fourni par l’application pour signaler la progression.                                                                                                    |
| [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | Installe un profil donné pour une utilisation sur un ordinateur spécifié. Le profil est également copié dans le répertoire des couleurs. |
| [**IsColorProfileTagPresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | Signale si une balise ICC (International Color Consortium) spécifiée est présente dans le profil de couleurs spécifié. |
| [**IsColorProfileValid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | permet de déterminer si le profil spécifié est un profil ICC (International color Consortium) valide ou un handle de profil WCS (Windows Color System) valide qui peut être utilisé pour la gestion des couleurs. |
| [**OpenColorProfileW**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | Crée un handle vers un profil de couleurs spécifié. Le descripteur peut ensuite être utilisé dans d’autres fonctions de gestion des profils. |
| [**RegisterCMMW**](/windows/win32/api/icm/nf-icm-registercmmw) | Associe une valeur d’identification spécifiée à la bibliothèque de liens dynamiques du module de gestion des couleurs spécifiée (DLL CMM). lorsque cet ID apparaît dans un profil de couleurs, Windows pouvez alors localiser le CMM correspondant afin de créer une transformation. |
| [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) | Vous permet de sélectionner le module de gestion des couleurs par défaut (CMM) à utiliser. |
| [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | Définit les données d’élément pour un élément de profil balisé dans un profil de couleurs ICC. |
| [**SetColorProfileElementReference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | Crée dans un profil de couleurs ICC spécifié une nouvelle balise qui référence les mêmes données qu’une balise existante. |
| [**SetColorProfileElementSize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | Définit la taille d’un élément balisé dans un profil de couleurs ICC. |
| [**SetColorProfileHeader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | Définit les données d’en-tête dans un profil de couleurs ICC spécifié. |
| [**SetColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                                                 | Définit l’espace colorimétrique d’entrée d’un contexte de périphérique.                                                                                                           |
| [**SetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | Définit la rampe gamma sur les panneaux d’affichage de couleur directe.                                                                                                  |
| [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                                       | Active ou désactive la gestion des couleurs dans un contexte de périphérique.                                                                                                |
| [**SetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                                                 | Définit le profil de couleur de sortie pour un contexte de périphérique donné.                                                                                            |
| [**SetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | Inscrit un profil spécifié pour un [espace de couleurs](c.md)standard donné. Le profil peut être interrogé à l’aide de [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew). |
| [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                                       | Fournit un contrôle utilisateur sur la gestion des couleurs par le biais d’une boîte de dialogue.                                                                                  |
| [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                                     | Convertit les couleurs de la bitmap à l’aide d’une transformation de couleur.                                                                                                      |
| [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) | Convertit un tableau de couleurs de l' [espace de couleurs](c.md) source en espace de couleurs de destination, tel que défini par une transformation de couleur. |
| [**UninstallColorProfileW**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | Supprime un profil de couleurs spécifié d’un ordinateur spécifié. Les fichiers associés sont éventuellement supprimés du système. |
| [**UnregisterCMMW**](/windows/win32/api/icm/nf-icm-unregistercmmw) | Dissocie une valeur d’ID spécifiée d’une bibliothèque de liens dynamiques (DLL) de module de gestion des couleurs donnée. |
| [**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | Associe un profil de couleurs WCS spécifié à un périphérique spécifié.                                                                                    |
| [**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                                               | Détermine si les couleurs d’un tableau se trouvent dans la gamme de sortie d’une transformation de couleur WCS spécifiée.                                            |
| [**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | Convertit un profil WCS en profil ICC.                                                                                                          |
| [**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | Dissocie un profil de couleurs WCS spécifié avec un périphérique spécifié sur un ordinateur spécifié.                                                         |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | Énumère tous les profils de couleurs qui répondent aux critères d’énumération dans la portée de gestion des profils spécifiée.                                       |
| [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize) | Retourne la taille, en octets, de la mémoire tampon requise par la fonction [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) pour énumérer les profils de couleurs. |
| [**WcsGetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | Détermine si la gestion du système de l’état d’étalonnage de l’affichage est activée.                                                                    |
| [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) | Récupère le profil de couleurs par défaut pour un appareil ou la valeur par défaut indépendante du périphérique si l’appareil n’est pas spécifié.                                  |
| [**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | Retourne la taille, en octets, du nom du profil de couleurs par défaut d’un appareil, y compris la marque de fin **null** .                                       |
| [**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Retourne l’intention de rendu au niveau de l’utilisateur ou du système.                                                                                                    |
| [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Détermine si l’utilisateur a choisi d’utiliser une liste d’association de profils par utilisateur pour l’appareil spécifié.                                          |
| [**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | Crée un handle vers un profil de couleurs spécifié.                                                                                                       |
| [**WcsSetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | Active ou désactive la gestion du système de l’état d’étalonnage de l’affichage.                                                                              |
| [**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | Définit le nom du profil de couleurs par défaut du type de profil spécifié dans l’étendue de gestion des profils spécifiée.                                         |
| [**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | Définit l’intention de rendu de l’utilisateur ou de l’ensemble du système.                                                                                                       |
| [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | Permet à l’utilisateur de spécifier s’il faut ou non utiliser une liste d’association de profils par utilisateur pour l’appareil spécifié.                                       |
| [**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | Convertit un tableau de couleurs de l’espace de couleurs source en espace de couleurs de destination, tel que défini par une transformation de couleur.                            |



 

 

 