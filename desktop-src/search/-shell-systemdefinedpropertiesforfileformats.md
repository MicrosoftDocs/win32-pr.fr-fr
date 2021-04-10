---
description: Microsoft Windows fournit un certain nombre de propriétés système que vous pouvez utiliser pour vos formats de fichiers.
ms.assetid: 3a25c4fb-ffea-4524-b59b-912416b2fc7d
title: Propriétés de System-Defined pour les formats de fichiers personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1a3645e383ea751298f766eacf60f5ac95ece3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112402"
---
# <a name="system-defined-properties-for-custom-file-formats"></a><span data-ttu-id="30d1a-103">Propriétés de System-Defined pour les formats de fichiers personnalisés</span><span class="sxs-lookup"><span data-stu-id="30d1a-103">System-Defined Properties for Custom File Formats</span></span>

<span data-ttu-id="30d1a-104">Microsoft Windows fournit un certain nombre de propriétés système que vous pouvez utiliser pour vos formats de fichiers.</span><span class="sxs-lookup"><span data-stu-id="30d1a-104">Microsoft Windows supplies a number of system properties that you can use for your file formats.</span></span> <span data-ttu-id="30d1a-105">Si vous créez un format de fichier personnalisé, vous devez prendre en charge autant de propriétés définies par le système que vous le pouvez.</span><span class="sxs-lookup"><span data-stu-id="30d1a-105">If you are creating a custom file format, you should support as many system-defined properties as you can.</span></span> <span data-ttu-id="30d1a-106">Avant de créer un gestionnaire de propriétés personnalisées, vous devez passer en revue les gestionnaires fournis par le système pour déterminer si vous pouvez en utiliser un au lieu d’écrire le vôtre.</span><span class="sxs-lookup"><span data-stu-id="30d1a-106">Before creating a custom property handler, you should review the system-supplied handlers to see if you can use one instead of writing your own.</span></span>

<span data-ttu-id="30d1a-107">Le tableau suivant classe les formats de fichiers, puis répertorie les propriétés système les plus importantes que votre format de fichier doit prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="30d1a-107">The following table categorizes file formats and then lists the most important system properties your file format should support.</span></span> <span data-ttu-id="30d1a-108">Pour offrir une expérience utilisateur optimale, vous devez prendre en charge toutes les propriétés de priorité 1 et 2 pour votre catégorie de format de fichier.</span><span class="sxs-lookup"><span data-stu-id="30d1a-108">To provide a good user experience, you should support all priority 1 and 2 properties for your category of file format.</span></span>

-   [<span data-ttu-id="30d1a-109">Communications</span><span class="sxs-lookup"><span data-stu-id="30d1a-109">Communications</span></span>](#communications)
-   [<span data-ttu-id="30d1a-110">Contacts</span><span class="sxs-lookup"><span data-stu-id="30d1a-110">Contacts</span></span>](#contacts)
-   [<span data-ttu-id="30d1a-111">Documents</span><span class="sxs-lookup"><span data-stu-id="30d1a-111">Documents</span></span>](#documents)
-   [<span data-ttu-id="30d1a-112">Générique</span><span class="sxs-lookup"><span data-stu-id="30d1a-112">Generic</span></span>](#generic)
-   [<span data-ttu-id="30d1a-113">Musicale</span><span class="sxs-lookup"><span data-stu-id="30d1a-113">Music</span></span>](#music)
-   [<span data-ttu-id="30d1a-114">Images</span><span class="sxs-lookup"><span data-stu-id="30d1a-114">Pictures</span></span>](#pictures)
-   [<span data-ttu-id="30d1a-115">Vidéos</span><span class="sxs-lookup"><span data-stu-id="30d1a-115">Videos</span></span>](#videos)
-   [<span data-ttu-id="30d1a-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="30d1a-116">Related topics</span></span>](#related-topics)

## <a name="communications"></a><span data-ttu-id="30d1a-117">Communications</span><span class="sxs-lookup"><span data-stu-id="30d1a-117">Communications</span></span>



| <span data-ttu-id="30d1a-118">Nom</span><span class="sxs-lookup"><span data-stu-id="30d1a-118">Name</span></span>            | <span data-ttu-id="30d1a-119">Propriété</span><span class="sxs-lookup"><span data-stu-id="30d1a-119">Property</span></span>                               | <span data-ttu-id="30d1a-120">Priority</span><span class="sxs-lookup"><span data-stu-id="30d1a-120">Priority</span></span> |
|-----------------|----------------------------------------|----------|
| <span data-ttu-id="30d1a-121">Date de réception</span><span class="sxs-lookup"><span data-stu-id="30d1a-121">Date received</span></span>   | <span data-ttu-id="30d1a-122">System. message. DateReceived</span><span class="sxs-lookup"><span data-stu-id="30d1a-122">System.Message.DateReceived</span></span>            | <span data-ttu-id="30d1a-123">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-123">1</span></span>        |
| <span data-ttu-id="30d1a-124">À partir de noms</span><span class="sxs-lookup"><span data-stu-id="30d1a-124">From names</span></span>      | <span data-ttu-id="30d1a-125">System. message. FromName</span><span class="sxs-lookup"><span data-stu-id="30d1a-125">System.Message.FromName</span></span>                | <span data-ttu-id="30d1a-126">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-126">1</span></span>        |
| <span data-ttu-id="30d1a-127">Contient des pièces jointes</span><span class="sxs-lookup"><span data-stu-id="30d1a-127">Has attachments</span></span> | <span data-ttu-id="30d1a-128">System. message. HasAttachments</span><span class="sxs-lookup"><span data-stu-id="30d1a-128">System.Message.HasAttachments</span></span>          | <span data-ttu-id="30d1a-129">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-129">1</span></span>        |
| <span data-ttu-id="30d1a-130">Mailbox</span><span class="sxs-lookup"><span data-stu-id="30d1a-130">Mailbox</span></span>         | <span data-ttu-id="30d1a-131">System. communication. storeddisplayname</span><span class="sxs-lookup"><span data-stu-id="30d1a-131">System.Communication.storeddisplayname</span></span> | <span data-ttu-id="30d1a-132">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-132">1</span></span>        |
| <span data-ttu-id="30d1a-133">Nom</span><span class="sxs-lookup"><span data-stu-id="30d1a-133">Name</span></span>            | <span data-ttu-id="30d1a-134">System. FileName</span><span class="sxs-lookup"><span data-stu-id="30d1a-134">System.FileName</span></span>                        | <span data-ttu-id="30d1a-135">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-135">1</span></span>        |
| <span data-ttu-id="30d1a-136">Objet</span><span class="sxs-lookup"><span data-stu-id="30d1a-136">Subject</span></span>         | <span data-ttu-id="30d1a-137">System. Subject</span><span class="sxs-lookup"><span data-stu-id="30d1a-137">System.Subject</span></span>                         | <span data-ttu-id="30d1a-138">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-138">1</span></span>        |
| <span data-ttu-id="30d1a-139">En noms</span><span class="sxs-lookup"><span data-stu-id="30d1a-139">To names</span></span>        | <span data-ttu-id="30d1a-140">System. message. ToName</span><span class="sxs-lookup"><span data-stu-id="30d1a-140">System.Message.ToName</span></span>                  | <span data-ttu-id="30d1a-141">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-141">1</span></span>        |
| <span data-ttu-id="30d1a-142">Category</span><span class="sxs-lookup"><span data-stu-id="30d1a-142">Category</span></span>        | <span data-ttu-id="30d1a-143">System. Category</span><span class="sxs-lookup"><span data-stu-id="30d1a-143">System.Category</span></span>                        | <span data-ttu-id="30d1a-144">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-144">2</span></span>        |
| <span data-ttu-id="30d1a-145">Type</span><span class="sxs-lookup"><span data-stu-id="30d1a-145">Type</span></span>            | <span data-ttu-id="30d1a-146">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="30d1a-146">System.PerceivedType</span></span>                   | <span data-ttu-id="30d1a-147">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-147">2</span></span>        |



 

## <a name="contacts"></a><span data-ttu-id="30d1a-148">Contacts</span><span class="sxs-lookup"><span data-stu-id="30d1a-148">Contacts</span></span>



| <span data-ttu-id="30d1a-149">Nom</span><span class="sxs-lookup"><span data-stu-id="30d1a-149">Name</span></span>             | <span data-ttu-id="30d1a-150">Propriété</span><span class="sxs-lookup"><span data-stu-id="30d1a-150">Property</span></span>                           | <span data-ttu-id="30d1a-151">Priority</span><span class="sxs-lookup"><span data-stu-id="30d1a-151">Priority</span></span> |
|------------------|------------------------------------|----------|
| <span data-ttu-id="30d1a-152">Nom du compte</span><span class="sxs-lookup"><span data-stu-id="30d1a-152">Account Name</span></span>     | <span data-ttu-id="30d1a-153">System. communication. AccountName</span><span class="sxs-lookup"><span data-stu-id="30d1a-153">System.Communication.AccountName</span></span>   | <span data-ttu-id="30d1a-154">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-154">1</span></span>        |
| <span data-ttu-id="30d1a-155">Téléphone professionnel</span><span class="sxs-lookup"><span data-stu-id="30d1a-155">Business Phone</span></span>   | <span data-ttu-id="30d1a-156">System. contact. BusinessTelephone</span><span class="sxs-lookup"><span data-stu-id="30d1a-156">System.Contact.BusinessTelephone</span></span>   | <span data-ttu-id="30d1a-157">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-157">1</span></span>        |
| <span data-ttu-id="30d1a-158">Company</span><span class="sxs-lookup"><span data-stu-id="30d1a-158">Company</span></span>          | <span data-ttu-id="30d1a-159">System. Company</span><span class="sxs-lookup"><span data-stu-id="30d1a-159">System.Company</span></span>                     | <span data-ttu-id="30d1a-160">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-160">1</span></span>        |
| <span data-ttu-id="30d1a-161">Adresse de messagerie</span><span class="sxs-lookup"><span data-stu-id="30d1a-161">Email Address</span></span>    | <span data-ttu-id="30d1a-162">System. contact. PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="30d1a-162">System.Contact.PrimaryEmailAddress</span></span> | <span data-ttu-id="30d1a-163">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-163">1</span></span>        |
| <span data-ttu-id="30d1a-164">importance</span><span class="sxs-lookup"><span data-stu-id="30d1a-164">Importance</span></span>       | <span data-ttu-id="30d1a-165">System. ImportanceText</span><span class="sxs-lookup"><span data-stu-id="30d1a-165">System.ImportanceText</span></span>              | <span data-ttu-id="30d1a-166">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-166">1</span></span>        |
| <span data-ttu-id="30d1a-167">Téléphone mobile</span><span class="sxs-lookup"><span data-stu-id="30d1a-167">Mobile Phone</span></span>     | <span data-ttu-id="30d1a-168">System. contact. MobileTelephone</span><span class="sxs-lookup"><span data-stu-id="30d1a-168">System.Contact.MobileTelephone</span></span>     | <span data-ttu-id="30d1a-169">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-169">1</span></span>        |
| <span data-ttu-id="30d1a-170">Adresse professionnelle</span><span class="sxs-lookup"><span data-stu-id="30d1a-170">Business address</span></span> | <span data-ttu-id="30d1a-171">System. contact. BusinessAddress</span><span class="sxs-lookup"><span data-stu-id="30d1a-171">System.Contact.BusinessAddress</span></span>     | <span data-ttu-id="30d1a-172">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-172">2</span></span>        |
| <span data-ttu-id="30d1a-173">Télécopie professionnelle</span><span class="sxs-lookup"><span data-stu-id="30d1a-173">Business fax</span></span>     | <span data-ttu-id="30d1a-174">System. contact. BusinessFaxNumber</span><span class="sxs-lookup"><span data-stu-id="30d1a-174">System.Contact.BusinessFaxNumber</span></span>   | <span data-ttu-id="30d1a-175">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-175">2</span></span>        |
| <span data-ttu-id="30d1a-176">Category</span><span class="sxs-lookup"><span data-stu-id="30d1a-176">Category</span></span>         | <span data-ttu-id="30d1a-177">System. Category</span><span class="sxs-lookup"><span data-stu-id="30d1a-177">System.Category</span></span>                    | <span data-ttu-id="30d1a-178">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-178">2</span></span>        |
| <span data-ttu-id="30d1a-179">Adresse personnelle</span><span class="sxs-lookup"><span data-stu-id="30d1a-179">Home address</span></span>     | <span data-ttu-id="30d1a-180">System. contact. HomeAddress</span><span class="sxs-lookup"><span data-stu-id="30d1a-180">System.Contact.HomeAddress</span></span>         | <span data-ttu-id="30d1a-181">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-181">2</span></span>        |
| <span data-ttu-id="30d1a-182">Téléphone personnel</span><span class="sxs-lookup"><span data-stu-id="30d1a-182">Home phone</span></span>       | <span data-ttu-id="30d1a-183">System. contact. HomeTelephone</span><span class="sxs-lookup"><span data-stu-id="30d1a-183">System.Contact.HomeTelephone</span></span>       | <span data-ttu-id="30d1a-184">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-184">2</span></span>        |
| <span data-ttu-id="30d1a-185">Intitulé</span><span class="sxs-lookup"><span data-stu-id="30d1a-185">Title</span></span>            | <span data-ttu-id="30d1a-186">System.Title</span><span class="sxs-lookup"><span data-stu-id="30d1a-186">System.Title</span></span>                       | <span data-ttu-id="30d1a-187">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-187">2</span></span>        |



 

## <a name="documents"></a><span data-ttu-id="30d1a-188">Documents</span><span class="sxs-lookup"><span data-stu-id="30d1a-188">Documents</span></span>



| <span data-ttu-id="30d1a-189">Nom</span><span class="sxs-lookup"><span data-stu-id="30d1a-189">Name</span></span>      | <span data-ttu-id="30d1a-190">Propriété</span><span class="sxs-lookup"><span data-stu-id="30d1a-190">Property</span></span>             | <span data-ttu-id="30d1a-191">Priority</span><span class="sxs-lookup"><span data-stu-id="30d1a-191">Priority</span></span> |
|-----------|----------------------|----------|
| <span data-ttu-id="30d1a-192">Auteurs</span><span class="sxs-lookup"><span data-stu-id="30d1a-192">Authors</span></span>   | <span data-ttu-id="30d1a-193">System.Author</span><span class="sxs-lookup"><span data-stu-id="30d1a-193">System.Author</span></span>        | <span data-ttu-id="30d1a-194">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-194">1</span></span>        |
| <span data-ttu-id="30d1a-195">Texte complet</span><span class="sxs-lookup"><span data-stu-id="30d1a-195">Full Text</span></span> | <span data-ttu-id="30d1a-196">System. FullText</span><span class="sxs-lookup"><span data-stu-id="30d1a-196">System.FullText</span></span>      | <span data-ttu-id="30d1a-197">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-197">1</span></span>        |
| <span data-ttu-id="30d1a-198">Balises</span><span class="sxs-lookup"><span data-stu-id="30d1a-198">Tags</span></span>      | <span data-ttu-id="30d1a-199">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="30d1a-199">System.Keywords</span></span>      | <span data-ttu-id="30d1a-200">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-200">1</span></span>        |
| <span data-ttu-id="30d1a-201">Type</span><span class="sxs-lookup"><span data-stu-id="30d1a-201">Type</span></span>      | <span data-ttu-id="30d1a-202">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="30d1a-202">System.PerceivedType</span></span> | <span data-ttu-id="30d1a-203">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-203">1</span></span>        |
| <span data-ttu-id="30d1a-204">Category</span><span class="sxs-lookup"><span data-stu-id="30d1a-204">Category</span></span>  | <span data-ttu-id="30d1a-205">System. Category</span><span class="sxs-lookup"><span data-stu-id="30d1a-205">System.Category</span></span>      | <span data-ttu-id="30d1a-206">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-206">2</span></span>        |
| <span data-ttu-id="30d1a-207">Intitulé</span><span class="sxs-lookup"><span data-stu-id="30d1a-207">Title</span></span>     | <span data-ttu-id="30d1a-208">System.Title</span><span class="sxs-lookup"><span data-stu-id="30d1a-208">System.Title</span></span>         | <span data-ttu-id="30d1a-209">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-209">2</span></span>        |



 

## <a name="generic"></a><span data-ttu-id="30d1a-210">Générique</span><span class="sxs-lookup"><span data-stu-id="30d1a-210">Generic</span></span>



| <span data-ttu-id="30d1a-211">Nom</span><span class="sxs-lookup"><span data-stu-id="30d1a-211">Name</span></span>     | <span data-ttu-id="30d1a-212">Propriété</span><span class="sxs-lookup"><span data-stu-id="30d1a-212">Property</span></span>             | <span data-ttu-id="30d1a-213">Priority</span><span class="sxs-lookup"><span data-stu-id="30d1a-213">Priority</span></span> |
|----------|----------------------|----------|
| <span data-ttu-id="30d1a-214">Auteurs</span><span class="sxs-lookup"><span data-stu-id="30d1a-214">Authors</span></span>  | <span data-ttu-id="30d1a-215">System.Author</span><span class="sxs-lookup"><span data-stu-id="30d1a-215">System.Author</span></span>        | <span data-ttu-id="30d1a-216">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-216">1</span></span>        |
| <span data-ttu-id="30d1a-217">Intitulé</span><span class="sxs-lookup"><span data-stu-id="30d1a-217">Title</span></span>    | <span data-ttu-id="30d1a-218">System.Title</span><span class="sxs-lookup"><span data-stu-id="30d1a-218">System.Title</span></span>         | <span data-ttu-id="30d1a-219">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-219">1</span></span>        |
| <span data-ttu-id="30d1a-220">Type</span><span class="sxs-lookup"><span data-stu-id="30d1a-220">Type</span></span>     | <span data-ttu-id="30d1a-221">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="30d1a-221">System.PerceivedType</span></span> | <span data-ttu-id="30d1a-222">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-222">1</span></span>        |
| <span data-ttu-id="30d1a-223">Category</span><span class="sxs-lookup"><span data-stu-id="30d1a-223">Category</span></span> | <span data-ttu-id="30d1a-224">System. Category</span><span class="sxs-lookup"><span data-stu-id="30d1a-224">System.Category</span></span>      | <span data-ttu-id="30d1a-225">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-225">2</span></span>        |
| <span data-ttu-id="30d1a-226">Balises</span><span class="sxs-lookup"><span data-stu-id="30d1a-226">Tags</span></span>     | <span data-ttu-id="30d1a-227">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="30d1a-227">System.Keywords</span></span>      | <span data-ttu-id="30d1a-228">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-228">2</span></span>        |



 

## <a name="music"></a><span data-ttu-id="30d1a-229">Musique</span><span class="sxs-lookup"><span data-stu-id="30d1a-229">Music</span></span>



| <span data-ttu-id="30d1a-230">Nom</span><span class="sxs-lookup"><span data-stu-id="30d1a-230">Name</span></span>         | <span data-ttu-id="30d1a-231">Propriété</span><span class="sxs-lookup"><span data-stu-id="30d1a-231">Property</span></span>                     | <span data-ttu-id="30d1a-232">Priority</span><span class="sxs-lookup"><span data-stu-id="30d1a-232">Priority</span></span> |
|--------------|------------------------------|----------|
| \#           | <span data-ttu-id="30d1a-233">System. Music. TrackNumber</span><span class="sxs-lookup"><span data-stu-id="30d1a-233">System.Music.TrackNumber</span></span>     | <span data-ttu-id="30d1a-234">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-234">1</span></span>        |
| <span data-ttu-id="30d1a-235">Album</span><span class="sxs-lookup"><span data-stu-id="30d1a-235">Album</span></span>        | <span data-ttu-id="30d1a-236">System. Music. AlbumTitle</span><span class="sxs-lookup"><span data-stu-id="30d1a-236">System.Music.AlbumTitle</span></span>      | <span data-ttu-id="30d1a-237">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-237">1</span></span>        |
| <span data-ttu-id="30d1a-238">Infographiste</span><span class="sxs-lookup"><span data-stu-id="30d1a-238">Artists</span></span>      | <span data-ttu-id="30d1a-239">System. Music. Artist</span><span class="sxs-lookup"><span data-stu-id="30d1a-239">System.Music.Artist</span></span>          | <span data-ttu-id="30d1a-240">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-240">1</span></span>        |
| <span data-ttu-id="30d1a-241">Genre</span><span class="sxs-lookup"><span data-stu-id="30d1a-241">Genre</span></span>        | <span data-ttu-id="30d1a-242">System. Music. genre</span><span class="sxs-lookup"><span data-stu-id="30d1a-242">System.Music.Genre</span></span>           | <span data-ttu-id="30d1a-243">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-243">1</span></span>        |
| <span data-ttu-id="30d1a-244">Rating</span><span class="sxs-lookup"><span data-stu-id="30d1a-244">Rating</span></span>       | <span data-ttu-id="30d1a-245">System. Rating</span><span class="sxs-lookup"><span data-stu-id="30d1a-245">System.Rating</span></span>                | <span data-ttu-id="30d1a-246">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-246">1</span></span>        |
| <span data-ttu-id="30d1a-247">Intitulé</span><span class="sxs-lookup"><span data-stu-id="30d1a-247">Title</span></span>        | <span data-ttu-id="30d1a-248">System.Title</span><span class="sxs-lookup"><span data-stu-id="30d1a-248">System.Title</span></span>                 | <span data-ttu-id="30d1a-249">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-249">1</span></span>        |
| <span data-ttu-id="30d1a-250">Artiste de l’album</span><span class="sxs-lookup"><span data-stu-id="30d1a-250">Album Artist</span></span> | <span data-ttu-id="30d1a-251">System. Music. AlbumArtist</span><span class="sxs-lookup"><span data-stu-id="30d1a-251">System.Music.AlbumArtist</span></span>     | <span data-ttu-id="30d1a-252">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-252">2</span></span>        |
| <span data-ttu-id="30d1a-253">Vitesse de transmission</span><span class="sxs-lookup"><span data-stu-id="30d1a-253">Bit Rate</span></span>     | <span data-ttu-id="30d1a-254">System. audio. EncodingBitrate</span><span class="sxs-lookup"><span data-stu-id="30d1a-254">System.Audio.EncodingBitrate</span></span> | <span data-ttu-id="30d1a-255">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-255">2</span></span>        |
| <span data-ttu-id="30d1a-256">Conductrices</span><span class="sxs-lookup"><span data-stu-id="30d1a-256">Conductors</span></span>   | <span data-ttu-id="30d1a-257">System. Music. conducteur</span><span class="sxs-lookup"><span data-stu-id="30d1a-257">System.Music.Conductor</span></span>       | <span data-ttu-id="30d1a-258">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-258">2</span></span>        |
| <span data-ttu-id="30d1a-259">Longueur</span><span class="sxs-lookup"><span data-stu-id="30d1a-259">Length</span></span>       | <span data-ttu-id="30d1a-260">System. Media. Duration</span><span class="sxs-lookup"><span data-stu-id="30d1a-260">System.Media.Duration</span></span>        | <span data-ttu-id="30d1a-261">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-261">2</span></span>        |
| <span data-ttu-id="30d1a-262">Protected</span><span class="sxs-lookup"><span data-stu-id="30d1a-262">Protected</span></span>    | <span data-ttu-id="30d1a-263">System. DRM. IsProtected</span><span class="sxs-lookup"><span data-stu-id="30d1a-263">System.DRM.IsProtected</span></span>       | <span data-ttu-id="30d1a-264">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-264">2</span></span>        |
| <span data-ttu-id="30d1a-265">Year</span><span class="sxs-lookup"><span data-stu-id="30d1a-265">Year</span></span>         | <span data-ttu-id="30d1a-266">System. Media. Year</span><span class="sxs-lookup"><span data-stu-id="30d1a-266">System.Media.Year</span></span>            | <span data-ttu-id="30d1a-267">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-267">2</span></span>        |



 

## <a name="pictures"></a><span data-ttu-id="30d1a-268">Images</span><span class="sxs-lookup"><span data-stu-id="30d1a-268">Pictures</span></span>



| <span data-ttu-id="30d1a-269">Nom</span><span class="sxs-lookup"><span data-stu-id="30d1a-269">Name</span></span>          | <span data-ttu-id="30d1a-270">Propriété</span><span class="sxs-lookup"><span data-stu-id="30d1a-270">Property</span></span>                        | <span data-ttu-id="30d1a-271">Priority</span><span class="sxs-lookup"><span data-stu-id="30d1a-271">Priority</span></span> |
|---------------|---------------------------------|----------|
| <span data-ttu-id="30d1a-272">Date d’importation</span><span class="sxs-lookup"><span data-stu-id="30d1a-272">Date imported</span></span> | <span data-ttu-id="30d1a-273">System. DateImported</span><span class="sxs-lookup"><span data-stu-id="30d1a-273">System.DateImported</span></span>             | <span data-ttu-id="30d1a-274">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-274">1</span></span>        |
| <span data-ttu-id="30d1a-275">Date de prise</span><span class="sxs-lookup"><span data-stu-id="30d1a-275">Date Taken</span></span>    | <span data-ttu-id="30d1a-276">System. photo. DateTaken</span><span class="sxs-lookup"><span data-stu-id="30d1a-276">System.Photo.DateTaken</span></span>          | <span data-ttu-id="30d1a-277">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-277">1</span></span>        |
| <span data-ttu-id="30d1a-278">Rating</span><span class="sxs-lookup"><span data-stu-id="30d1a-278">Rating</span></span>        | <span data-ttu-id="30d1a-279">System. Rating</span><span class="sxs-lookup"><span data-stu-id="30d1a-279">System.Rating</span></span>                   | <span data-ttu-id="30d1a-280">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-280">1</span></span>        |
| <span data-ttu-id="30d1a-281">Balises</span><span class="sxs-lookup"><span data-stu-id="30d1a-281">Tags</span></span>          | <span data-ttu-id="30d1a-282">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="30d1a-282">System.Keywords</span></span>                 | <span data-ttu-id="30d1a-283">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-283">1</span></span>        |
| <span data-ttu-id="30d1a-284">Type</span><span class="sxs-lookup"><span data-stu-id="30d1a-284">Type</span></span>          | <span data-ttu-id="30d1a-285">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="30d1a-285">System.PerceivedType</span></span>            | <span data-ttu-id="30d1a-286">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-286">1</span></span>        |
| <span data-ttu-id="30d1a-287">Auteurs</span><span class="sxs-lookup"><span data-stu-id="30d1a-287">Authors</span></span>       | <span data-ttu-id="30d1a-288">System.Author</span><span class="sxs-lookup"><span data-stu-id="30d1a-288">System.Author</span></span>                   | <span data-ttu-id="30d1a-289">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-289">2</span></span>        |
| <span data-ttu-id="30d1a-290">Fabricant de l’appareil photo</span><span class="sxs-lookup"><span data-stu-id="30d1a-290">Camera maker</span></span>  | <span data-ttu-id="30d1a-291">System. photo. CameraManufacturer</span><span class="sxs-lookup"><span data-stu-id="30d1a-291">System.Photo.CameraManufacturer</span></span> | <span data-ttu-id="30d1a-292">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-292">2</span></span>        |
| <span data-ttu-id="30d1a-293">Modèle d’appareil photo</span><span class="sxs-lookup"><span data-stu-id="30d1a-293">Camera model</span></span>  | <span data-ttu-id="30d1a-294">System. photo. CameraModel</span><span class="sxs-lookup"><span data-stu-id="30d1a-294">System.Photo.CameraModel</span></span>        | <span data-ttu-id="30d1a-295">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-295">2</span></span>        |
| <span data-ttu-id="30d1a-296">Commentaires</span><span class="sxs-lookup"><span data-stu-id="30d1a-296">Comments</span></span>      | <span data-ttu-id="30d1a-297">System. Comment</span><span class="sxs-lookup"><span data-stu-id="30d1a-297">System.Comment</span></span>                  | <span data-ttu-id="30d1a-298">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-298">2</span></span>        |
| <span data-ttu-id="30d1a-299">Dimensions</span><span class="sxs-lookup"><span data-stu-id="30d1a-299">Dimensions</span></span>    | <span data-ttu-id="30d1a-300">System. image. Dimensions</span><span class="sxs-lookup"><span data-stu-id="30d1a-300">System.Image.Dimensions</span></span>         | <span data-ttu-id="30d1a-301">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-301">2</span></span>        |



 

## <a name="videos"></a><span data-ttu-id="30d1a-302">Vidéos</span><span class="sxs-lookup"><span data-stu-id="30d1a-302">Videos</span></span>



| <span data-ttu-id="30d1a-303">Nom</span><span class="sxs-lookup"><span data-stu-id="30d1a-303">Name</span></span>         | <span data-ttu-id="30d1a-304">Propriété</span><span class="sxs-lookup"><span data-stu-id="30d1a-304">Property</span></span>                 | <span data-ttu-id="30d1a-305">Priority</span><span class="sxs-lookup"><span data-stu-id="30d1a-305">Priority</span></span> |
|--------------|--------------------------|----------|
| <span data-ttu-id="30d1a-306">Longueur</span><span class="sxs-lookup"><span data-stu-id="30d1a-306">Length</span></span>       | <span data-ttu-id="30d1a-307">System. Media. Duration</span><span class="sxs-lookup"><span data-stu-id="30d1a-307">System.Media.Duration</span></span>    | <span data-ttu-id="30d1a-308">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-308">1</span></span>        |
| <span data-ttu-id="30d1a-309">Rating</span><span class="sxs-lookup"><span data-stu-id="30d1a-309">Rating</span></span>       | <span data-ttu-id="30d1a-310">System. Rating</span><span class="sxs-lookup"><span data-stu-id="30d1a-310">System.Rating</span></span>            | <span data-ttu-id="30d1a-311">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-311">1</span></span>        |
| <span data-ttu-id="30d1a-312">Balises</span><span class="sxs-lookup"><span data-stu-id="30d1a-312">Tags</span></span>         | <span data-ttu-id="30d1a-313">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="30d1a-313">System.Keywords</span></span>          | <span data-ttu-id="30d1a-314">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-314">1</span></span>        |
| <span data-ttu-id="30d1a-315">Type</span><span class="sxs-lookup"><span data-stu-id="30d1a-315">Type</span></span>         | <span data-ttu-id="30d1a-316">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="30d1a-316">System.PerceivedType</span></span>     | <span data-ttu-id="30d1a-317">1</span><span class="sxs-lookup"><span data-stu-id="30d1a-317">1</span></span>        |
| <span data-ttu-id="30d1a-318">Hauteur du frame</span><span class="sxs-lookup"><span data-stu-id="30d1a-318">Frame height</span></span> | <span data-ttu-id="30d1a-319">System. Video. FrameHeight</span><span class="sxs-lookup"><span data-stu-id="30d1a-319">System.Video.FrameHeight</span></span> | <span data-ttu-id="30d1a-320">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-320">2</span></span>        |
| <span data-ttu-id="30d1a-321">Largeur du cadre</span><span class="sxs-lookup"><span data-stu-id="30d1a-321">Frame width</span></span>  | <span data-ttu-id="30d1a-322">System. Video. FrameWidth</span><span class="sxs-lookup"><span data-stu-id="30d1a-322">System.Video.FrameWidth</span></span>  | <span data-ttu-id="30d1a-323">2</span><span class="sxs-lookup"><span data-stu-id="30d1a-323">2</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="30d1a-324">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="30d1a-324">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="30d1a-325">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="30d1a-325">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="30d1a-326">Développement de gestionnaires de propriétés pour Windows Search</span><span class="sxs-lookup"><span data-stu-id="30d1a-326">Developing Property Handlers for Windows Search</span></span>](-search-3x-wds-extidx-propertyhandlers.md)
</dt> <dt>

<span data-ttu-id="30d1a-327">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="30d1a-327">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="30d1a-328">Système de propriétés</span><span class="sxs-lookup"><span data-stu-id="30d1a-328">Property System</span></span>](../properties/building-property-handlers.md)
</dt> <dt>

<span data-ttu-id="30d1a-329">[Propriétés système](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="30d1a-329">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> </dl>

 

 
