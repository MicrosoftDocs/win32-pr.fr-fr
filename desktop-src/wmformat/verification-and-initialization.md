---
title: Vérification et initialisation
description: Vérification et initialisation
ms.assetid: e92abaa2-0bac-4c78-bda7-d118c4f5b332
keywords:
- Windows Media Format SDK, vérification
- Windows Media Format SDK, initialisation
- gestion des droits numériques (DRM), vérification
- DRM (gestion des droits numériques), vérification
- gestion des droits numériques (DRM), initialisation
- DRM (gestion des droits numériques), initialisation
- API étendues du client DRM, vérification
- API étendues du client, vérification
- API étendues du client DRM, initialisation
- API étendues du client, initialisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59c54b56e0622fb65a1a57ae1909e0e6e64aaca6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314311"
---
# <a name="verification-and-initialization"></a><span data-ttu-id="3c60c-113">Vérification et initialisation</span><span class="sxs-lookup"><span data-stu-id="3c60c-113">Verification and Initialization</span></span>

<span data-ttu-id="3c60c-114">Vous devez effectuer les étapes suivantes pour vérifier que la transchiffrement est autorisée et initialiser un objet qui déchiffrera le contenu :</span><span class="sxs-lookup"><span data-stu-id="3c60c-114">You should perform the following steps to verify that transcryption is allowed and to initialize an object that will decrypt the content:</span></span>

1.  <span data-ttu-id="3c60c-115">Si vous avez déjà l’ID de clé du contenu, passez à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="3c60c-115">If you already have the Key ID for the content, skip to step 5.</span></span>
2.  <span data-ttu-id="3c60c-116">Appelez la fonction [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) pour créer un objet d’éditeur de métadonnées et obtenir une instance de l’interface [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) de cet objet.</span><span class="sxs-lookup"><span data-stu-id="3c60c-116">Call the [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) function to create a metadata editor object and get an instance of that object's [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) interface.</span></span>
3.  <span data-ttu-id="3c60c-117">Appelez **IWMMetadataEditor :: QueryInterface** pour récupérer une instance de l’interface [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) .</span><span class="sxs-lookup"><span data-stu-id="3c60c-117">Call **IWMMetadataEditor::QueryInterface** to get an instance of the [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) interface.</span></span>
4.  <span data-ttu-id="3c60c-118">Appelez [**IWMDRMEditor :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) pour accéder à la propriété **DRM \_ DRMHeader \_ KeyId** .</span><span class="sxs-lookup"><span data-stu-id="3c60c-118">Call [**IWMDRMEditor::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) to get the **DRM\_DRMHeader\_KeyID** property.</span></span>
5.  <span data-ttu-id="3c60c-119">Initialisez les API étendues du client Windows Media DRM en appelant la fonction [**WMDRMStartup**](wmdrmstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="3c60c-119">Initialize the Windows Media DRM Client Extended APIs by calling the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span>
6.  <span data-ttu-id="3c60c-120">Appelez la fonction [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) pour créer un objet fournisseur sécurisé et obtenir une instance de l’interface [**IWMDRMProvider**](iwmdrmprovider.md) de cet objet.</span><span class="sxs-lookup"><span data-stu-id="3c60c-120">Call the [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) function to create a secure provider object and get an instance of that object's [**IWMDRMProvider**](iwmdrmprovider.md) interface.</span></span>
7.  <span data-ttu-id="3c60c-121">Appelez [**IWMDRMProvider :: CreateObject**](iwmdrmprovider-createobject.md) pour créer un objet de gestion de licences et obtenir une instance de son interface [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) .</span><span class="sxs-lookup"><span data-stu-id="3c60c-121">Call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md) to create a license management object and get an instance of its [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) interface.</span></span>
8.  <span data-ttu-id="3c60c-122">Appelez [**IWMDRMLicenseManagement :: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), en passant l’ID de la clé et le droit qui régit les actions à effectuer avec le contenu après qu’il a été chiffré.</span><span class="sxs-lookup"><span data-stu-id="3c60c-122">Call [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passing in the Key ID and the right that governs the actions to be taken with the content after it is transcrypted.</span></span> <span data-ttu-id="3c60c-123">Cet appel permet de récupérer une instance de l’interface [**IWMDRMLicense**](iwmdrmlicense.md) qui peut être utilisée pour énumérer toutes les licences correspondantes.</span><span class="sxs-lookup"><span data-stu-id="3c60c-123">This call will retrieve an instance of the [**IWMDRMLicense**](iwmdrmlicense.md) interface that can be used to enumerate through any matching licenses.</span></span>
9.  <span data-ttu-id="3c60c-124">Appelez [**IWMDRMLicense :: GetInclusionList**](iwmdrmlicense-getinclusionlist.md) pour récupérer la liste des systèmes de protection de contenu (CPS) autorisés, comme spécifié par l’émetteur de licence.</span><span class="sxs-lookup"><span data-stu-id="3c60c-124">Call [**IWMDRMLicense::GetInclusionList**](iwmdrmlicense-getinclusionlist.md) to retrieve the list of authorized content protection systems (CPS) as specified by the license issuer.</span></span>
10. <span data-ttu-id="3c60c-125">Analyser la liste d’inclusion pour confirmer que le GUID de la sortie CPS est autorisé par la licence.</span><span class="sxs-lookup"><span data-stu-id="3c60c-125">Parse the inclusion list to confirm that the GUID of the output CPS is allowed by the license.</span></span>
11. <span data-ttu-id="3c60c-126">Si le GUID d’exportation souhaité ne figure pas dans la liste d’inclusion, appelez [**IWMDRMLicense :: GetNext**](iwmdrmlicense-getnext.md) pour accéder à la prochaine licence applicable (le cas échéant) et répétez les étapes 9 et 10.</span><span class="sxs-lookup"><span data-stu-id="3c60c-126">If the desired export GUID is not in the inclusion list, call [**IWMDRMLicense::GetNext**](iwmdrmlicense-getnext.md) to get the next applicable license (if any) and repeat steps 9 and 10.</span></span> <span data-ttu-id="3c60c-127">Si aucune licence n’a le GUID souhaité dans sa liste d’inclusion, l’exportation ne peut pas être effectuée.</span><span class="sxs-lookup"><span data-stu-id="3c60c-127">If no license has the desired GUID in its inclusion list, the export cannot be performed.</span></span>
12. <span data-ttu-id="3c60c-128">Appelez [**IWMDRMLicense :: CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md) pour créer un objet déchiffreur.</span><span class="sxs-lookup"><span data-stu-id="3c60c-128">Call [**IWMDRMLicense::CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md) to create a decryptor object.</span></span> <span data-ttu-id="3c60c-129">Transmettez le certificat d’application d’exportation.</span><span class="sxs-lookup"><span data-stu-id="3c60c-129">Pass in the export application certificate.</span></span> <span data-ttu-id="3c60c-130">Cet appel fournira un pointeur vers une instance de l’interface [**IWMDRMDecrypt**](iwmdrmdecrypt.md) de l’objet déchiffreur et un objet binaire contenant la valeur initiale.</span><span class="sxs-lookup"><span data-stu-id="3c60c-130">This call will provide a pointer to an instance of the decryptor object's [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface and a binary object containing the seed.</span></span> <span data-ttu-id="3c60c-131">Seule la constante **RC4 du \_ \_ type de \_ protection DRM** Windows Media est prise en charge en tant qu’argument du paramètre *dwFlags* pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="3c60c-131">Only the Windows Media **DRM\_PROTECTION\_TYPE\_RC4** constant is supported as an argument to the *dwFlags* parameter at this time.</span></span>
13. <span data-ttu-id="3c60c-132">Utilisez le schéma de chiffrement OAEP RSA pour déchiffrer le vecteur d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="3c60c-132">Use the RSA OAEP encryption scheme to decrypt the initialization vector.</span></span>
14. <span data-ttu-id="3c60c-133">Utilisez la bibliothèque d’analyse ASF fournie par Microsoft lorsque vous entrez dans le contrat d’exportation DRM Windows Media, afin de localiser le décalage en octets pour chaque charge utile.</span><span class="sxs-lookup"><span data-stu-id="3c60c-133">Use the ASF parsing library provided by Microsoft when you enter into the Windows Media DRM export agreement, to locate the offset in bytes for each payload.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c60c-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3c60c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c60c-135">**Exportation du contenu compressé**</span><span class="sxs-lookup"><span data-stu-id="3c60c-135">**Exporting Compressed Content**</span></span>](exporting-compressed-content.md)
</dt> </dl>

 

 




