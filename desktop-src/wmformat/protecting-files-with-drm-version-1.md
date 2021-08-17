---
title: Protection des fichiers avec DRM version 1
description: Protection des fichiers avec DRM version 1
ms.assetid: 91de1c20-e926-4ff6-b0cd-e90fc9cbaad2
keywords:
- Windows Media Format SDK, création de fichiers protégés
- Windows Media Format SDK, fichiers protégés
- ASF (Advanced Systems Format), création de fichiers protégés
- ASF (format des systèmes avancés), création de fichiers protégés
- ASF (Advanced Systems Format), fichiers protégés
- ASF (Advanced Systems Format), fichiers protégés
- ASF (Advanced Systems Format), WMStubDRM. lib
- ASF (format avancé des systèmes), WMStubDRM. lib
- WMStubDRM. lib, création de fichiers protégés
- WMStubDRM. lib, fichiers protégés
- gestion des droits numériques (DRM), WMStubDRM. lib
- DRM (gestion des droits numériques), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b500f3711b8c92324cbd87d4dc199a8a0bb803cba69357a23f139fb96f8281f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084536"
---
# <a name="protecting-files-with-drm-version-1"></a>Protection des fichiers avec DRM version 1

Lorsque ce type de protection est appliqué, une licence DRM version 1 est générée et valide uniquement sur l’ordinateur à partir duquel la demande de licence a été effectuée. Étant donné qu’aucune clé ou valeur initiale de clé n’est définie, il n’existe aucun moyen de générer des licences portables pour le contenu protégé à l’aide de cette technique. toutefois, lors de l’utilisation de Windows Media Format SDK 7,1 ou version ultérieure, les licences sont récupérables par le service de Migration de licences Microsoft.

Pour protéger des fichiers ASF à l’aide de DRM version 1, procédez comme suit :

1.  Liez le fichier WMStubDRM. lib à votre projet et, si nécessaire, dissociez wmvcore. lib.
2.  Appelez la fonction [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) pour créer le writer. Le premier argument est réservé et doit avoir la valeur **null**.
3.  Définissez un profil que le writer doit utiliser en appelant [**IWMWriter :: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) ou [**IWMWriter :: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid). Vous devez définir un profil dans l’enregistreur avant de définir des attributs DRM. DRM est pris en charge uniquement pour les profils qui utilisent les codecs Windows Media Audio ou Windows Media Video.
4.  À l’aide de la méthode [**IWMHeaderInfo :: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) , définissez les propriétés DRM suivantes. La propriété utiliser la gestion des **\_ droits numériques (DRM** ) demande aux composants DRM de protéger le contenu à l’aide de DRM version 1. La **propriété \_ indicateurs DRM** spécifie les droits à inclure dans la licence locale qui sera créée pour le contenu. La valeur de **\_ niveau DRM** est également stockée dans la licence. elle spécifie le niveau minimal requis pour accéder au contenu. 150 est le niveau recommandé pour le contenu DRM version 1.

    | Attribut      | Valeur                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | **Utiliser \_ DRM**   | **TRUE**                                                                                    |
    | **\_Indicateurs DRM** | lecture à la bonne lecture WMT droit \_ \_ \| de la \_ \_ copie vers un \_ \_ \_ appareil non \_ -SDMI \| \_ \_ copie appropriée sur le \_ \_ CD |
    | **\_niveau DRM** | 150                                                                                         |

    

     

L’exemple de code suivant montre comment créer un enregistreur DRM pour DRM version 1 et définir les propriétés DRM. La vérification des erreurs a été omise pour des raisons de clarification.


```C++
BOOL  fUseDRM    = TRUE;
// These are the rights we will apply to the file. See WMT_RIGHTS for
// the full set of possible rights.

DWORD dwDRMFlags = WMT_RIGHT_PLAYBACK | 
                   WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE | 
                   WMT_RIGHT_COPY_TO_CD;

// Set the minimum required DRM level low enough
// to allow older players to access the content.
DWORD dwDRMLevel = 150;

IWMDRMWriter*  pWMDRMWriter  = NULL;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer object.
hr = WMCreateWriter( NULL, &pWMDRMWriter);

// Obtain the IWMHeaderInfo interface.
hr = pWMDRMWriter -> QueryInterface(IID_IWMHeaderInfo, 
                                   (void**) &pWMHeaderInfo);

// Tell the SDK runtime to protect the file using DRM version 1.
hr= pWMHeaderInfo-> SetAttribute(0,
                                 g_wszWMUse_DRM,
                                 WMT_TYPE_BOOL,
                                 (BYTE*)&fUseDRM,
                                 sizeof(BOOL));

// Specify the rights that will be stored in the local license that is
// created automatically for the content.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Flags, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMFlags,
                                 sizeof(DWORD) );

// Set the DRM_Level attribute in the file's DRM header.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Level, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMLevel,
                                 sizeof(DWORD) );
```



 

 




