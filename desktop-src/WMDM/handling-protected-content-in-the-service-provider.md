---
title: Gestion du contenu protégé dans le fournisseur de services
description: Gestion du contenu protégé dans le fournisseur de services
ms.assetid: 5c18c8ec-d579-41df-8c25-c143fb9cdbef
keywords:
- Gestionnaire de périphériques Windows Media, certificats
- Gestionnaire de périphériques, certificats
- Guide de programmation, certificats
- fournisseurs de services, certificats
- création de fournisseurs de services, certificats
- certificates
- Gestionnaire de périphériques Windows Media, contenu protégé par DRM
- Gestionnaire de périphériques, contenu protégé par DRM
- Guide de programmation, contenu protégé par DRM
- fournisseurs de services, contenu protégé par DRM
- création de fournisseurs de services, contenu protégé par DRM
- Contenu protégé par DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d10cf9078cf9aaf631b65de968f01491a97781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510400"
---
# <a name="handling-protected-content-in-the-service-provider"></a><span data-ttu-id="53d08-115">Gestion du contenu protégé dans le fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="53d08-115">Handling Protected Content in the Service Provider</span></span>

<span data-ttu-id="53d08-116">Vous pouvez créer un fournisseur de services qui peut envoyer du contenu protégé par DRM à un appareil basé sur des DRM d’appareils mobiles (PDDRM), mais vous ne pouvez pas créer un fournisseur de services qui peut envoyer du contenu protégé par DRM à des appareils basés sur Windows Media DRM 10 pour les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="53d08-116">You can build a service provider that can send DRM-protected content to a device built on Portable Device DRM (PDDRM), but you cannot build a service provider that can send DRM-protected content to devices built on Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="53d08-117">Ces appareils utilisent MTP et vous ne pouvez pas créer votre propre fournisseur de services MTP.</span><span class="sxs-lookup"><span data-stu-id="53d08-117">These devices use MTP, and you cannot build your own MTP service provider.</span></span>

<span data-ttu-id="53d08-118">La seule étape supplémentaire qu’un fournisseur de services doit effectuer pour envoyer un matériel DRM à un appareil PDDRM consiste à obtenir un certificat/une paire de clés émis par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="53d08-118">The only extra step that a service provider must take to send DRM material to a PDDRM device is to get a Microsoft-issued certificate/key pair.</span></span> <span data-ttu-id="53d08-119">Pour savoir où obtenir ce certificat ou cette clé, consultez [outils de développement](tools-for-development.md) .</span><span class="sxs-lookup"><span data-stu-id="53d08-119">See [Tools for Development](tools-for-development.md) to learn where to get this certificate/key.</span></span> <span data-ttu-id="53d08-120">Les licences émises pour ces appareils seront des licences simplifiées qui prennent uniquement en charge la lecture simple du contenu acheté. ils ne prennent pas en charge les licences d’expiration temporelles.</span><span class="sxs-lookup"><span data-stu-id="53d08-120">The licenses issued to these devices will be simplified licenses that only support simple playback of purchased content; they will not support time-expiring licenses.</span></span> <span data-ttu-id="53d08-121">Cette licence sera créée pour vous par le fournisseur de contenu sécurisé (fourni par Microsoft pour les fichiers WMA/WMV) et stockée dans l’en-tête du fichier envoyé au fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="53d08-121">This license will be created for you by the secure content provider (provided by Microsoft for WMA/WMV files) and stored in the header of the file sent to the service provider.</span></span> <span data-ttu-id="53d08-122">Vous n’aurez pas à effectuer d’étapes spéciales pour les fichiers protégés.</span><span class="sxs-lookup"><span data-stu-id="53d08-122">You will not have to take any special steps for protected files.</span></span>

<span data-ttu-id="53d08-123">Une fois le fichier protégé envoyé, Windows Media Gestionnaire de périphériques appelle le fournisseur de services pour demander un fichier de stockage de licence spécial à partir de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="53d08-123">After sending the protected file, Windows Media Device Manager will call the service provider to request a special license storage file from the device.</span></span> <span data-ttu-id="53d08-124">Windows Media Gestionnaire de périphériques ajoute une copie de la nouvelle licence à ce fichier et le renvoie au fournisseur de services pour le renvoyer à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="53d08-124">Windows Media Device Manager will add a copy of the new license to this file, and return it to the service provider to send back to the device.</span></span> <span data-ttu-id="53d08-125">Toutefois, même si le fournisseur de services ne parvient pas à trouver ou à retourner ce fichier, il doit toujours être en mesure de lire le fichier protégé à l’aide de la copie de licence dans l’en-tête de fichier.</span><span class="sxs-lookup"><span data-stu-id="53d08-125">However, even if the service provider fails to find or return this file, the device should still be able to play the protected file by using the license copy in the file header.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53d08-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="53d08-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53d08-127">**Création d’un fournisseur de services**</span><span class="sxs-lookup"><span data-stu-id="53d08-127">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> <dt>

[<span data-ttu-id="53d08-128">**Gestion du contenu protégé**</span><span class="sxs-lookup"><span data-stu-id="53d08-128">**Handling Protected Content**</span></span>](handling-protected-content.md)
</dt> </dl>

 

 




