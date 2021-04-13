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
ms.openlocfilehash: 1d3e4d1ae9c0d3835c20f75b4e61c262a85a26f4
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314516"
---
# <a name="protecting-files-with-drm-version-1"></a><span data-ttu-id="15bda-115">Protection des fichiers avec DRM version 1</span><span class="sxs-lookup"><span data-stu-id="15bda-115">Protecting Files with DRM Version 1</span></span>

<span data-ttu-id="15bda-116">Lorsque ce type de protection est appliqué, une licence DRM version 1 est générée et valide uniquement sur l’ordinateur à partir duquel la demande de licence a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="15bda-116">When this kind of protection is applied, a DRM version 1 license is generated that is valid only on the machine from which the license request was made.</span></span> <span data-ttu-id="15bda-117">Étant donné qu’aucune clé ou valeur initiale de clé n’est définie, il n’existe aucun moyen de générer des licences portables pour le contenu protégé à l’aide de cette technique.</span><span class="sxs-lookup"><span data-stu-id="15bda-117">Because no key or key seed is set, there is no way to generate portable licenses for content protected using this technique.</span></span> <span data-ttu-id="15bda-118">Toutefois, lorsque vous utilisez le kit de développement logiciel (SDK) Windows Media Format 7,1 ou une version ultérieure, les licences sont récupérables dans le service de migration de licences Microsoft.</span><span class="sxs-lookup"><span data-stu-id="15bda-118">However, when using the Windows Media Format SDK 7.1 or later, the licenses are recoverable at the Microsoft License Migration service.</span></span>

<span data-ttu-id="15bda-119">Pour protéger des fichiers ASF à l’aide de DRM version 1, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="15bda-119">To protect ASF files using DRM version 1, perform the following steps:</span></span>

1.  <span data-ttu-id="15bda-120">Liez le fichier WMStubDRM. lib à votre projet et, si nécessaire, dissociez wmvcore. lib.</span><span class="sxs-lookup"><span data-stu-id="15bda-120">Link the WMStubDRM.lib file to your project and, if necessary, unlink wmvcore.lib.</span></span>
2.  <span data-ttu-id="15bda-121">Appelez la fonction [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) pour créer le writer.</span><span class="sxs-lookup"><span data-stu-id="15bda-121">Call the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function to create the writer.</span></span> <span data-ttu-id="15bda-122">Le premier argument est réservé et doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="15bda-122">The first argument is reserved and must be set to **NULL**.</span></span>
3.  <span data-ttu-id="15bda-123">Définissez un profil que le writer doit utiliser en appelant [**IWMWriter :: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) ou [**IWMWriter :: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid).</span><span class="sxs-lookup"><span data-stu-id="15bda-123">Set a profile for the writer to use by calling [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) or [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid).</span></span> <span data-ttu-id="15bda-124">Vous devez définir un profil dans l’enregistreur avant de définir des attributs DRM.</span><span class="sxs-lookup"><span data-stu-id="15bda-124">You must set a profile in the writer before setting any DRM attributes.</span></span> <span data-ttu-id="15bda-125">DRM est pris en charge uniquement pour les profils qui utilisent les codecs Windows Media Audio ou Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="15bda-125">DRM is supported only for profiles that use the Windows Media Audio or Windows Media Video codecs.</span></span>
4.  <span data-ttu-id="15bda-126">À l’aide de la méthode [**IWMHeaderInfo :: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) , définissez les propriétés DRM suivantes.</span><span class="sxs-lookup"><span data-stu-id="15bda-126">Using the [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) method, set the following DRM properties.</span></span> <span data-ttu-id="15bda-127">La propriété utiliser la gestion des **\_ droits numériques (DRM** ) demande aux composants DRM de protéger le contenu à l’aide de DRM version 1.</span><span class="sxs-lookup"><span data-stu-id="15bda-127">The **Use\_DRM** property instructs the DRM components to protect the content using DRM version 1.</span></span> <span data-ttu-id="15bda-128">La **propriété \_ indicateurs DRM** spécifie les droits à inclure dans la licence locale qui sera créée pour le contenu.</span><span class="sxs-lookup"><span data-stu-id="15bda-128">The **DRM\_Flags** property specifies the rights to be included in the local license that will be created for the content.</span></span> <span data-ttu-id="15bda-129">La valeur de **\_ niveau DRM** est également stockée dans la licence. elle spécifie le niveau minimal requis pour accéder au contenu.</span><span class="sxs-lookup"><span data-stu-id="15bda-129">The **DRM\_LEVEL** value is also stored in the license; it specifies the minimum level required to access the content.</span></span> <span data-ttu-id="15bda-130">150 est le niveau recommandé pour le contenu DRM version 1.</span><span class="sxs-lookup"><span data-stu-id="15bda-130">150 is the recommended level for DRM version 1 content.</span></span>

    | <span data-ttu-id="15bda-131">Attribut</span><span class="sxs-lookup"><span data-stu-id="15bda-131">Attribute</span></span>      | <span data-ttu-id="15bda-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="15bda-132">Value</span></span>                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | <span data-ttu-id="15bda-133">**Utiliser \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="15bda-133">**Use\_DRM**</span></span>   | <span data-ttu-id="15bda-134">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="15bda-134">**TRUE**</span></span>                                                                                    |
    | <span data-ttu-id="15bda-135">**\_Indicateurs DRM**</span><span class="sxs-lookup"><span data-stu-id="15bda-135">**DRM\_Flags**</span></span> | <span data-ttu-id="15bda-136">lecture à la bonne lecture WMT droit \_ \_ \| de la \_ \_ copie vers un \_ \_ \_ appareil non \_ -SDMI \| \_ \_ copie appropriée sur le \_ \_ CD</span><span class="sxs-lookup"><span data-stu-id="15bda-136">WMT\_RIGHT\_PLAYBACK \| WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE \| WMT\_RIGHT\_COPY\_TO\_CD</span></span> |
    | <span data-ttu-id="15bda-137">**\_niveau DRM**</span><span class="sxs-lookup"><span data-stu-id="15bda-137">**DRM\_LEVEL**</span></span> | <span data-ttu-id="15bda-138">150</span><span class="sxs-lookup"><span data-stu-id="15bda-138">150</span></span>                                                                                         |

    

     

<span data-ttu-id="15bda-139">L’exemple de code suivant montre comment créer un enregistreur DRM pour DRM version 1 et définir les propriétés DRM.</span><span class="sxs-lookup"><span data-stu-id="15bda-139">The following example code shows how to create a DRM-enabled writer for DRM version 1 and set the DRM properties.</span></span> <span data-ttu-id="15bda-140">La vérification des erreurs a été omise pour des raisons de clarification.</span><span class="sxs-lookup"><span data-stu-id="15bda-140">Error checking has been omitted for the sake of clarify.</span></span>


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



 

 




