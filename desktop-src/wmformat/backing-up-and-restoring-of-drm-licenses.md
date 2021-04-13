---
title: Sauvegarde et restauration de licences DRM
description: Sauvegarde et restauration de licences DRM
ms.assetid: ec2777e9-76af-43fe-8bd5-4d7532d2fb32
keywords:
- Windows Media Format SDK, sauvegarde des licences DRM
- Windows Media Format SDK, restauration de licences DRM
- Windows Media Format SDK, licences DRM
- Windows Media Format SDK, licences pour DRM
- Windows Media Format SDK, fonctionnalité de restauration de sauvegarde
- Windows Media Format SDK, service de gestion des licences
- Windows Media Format SDK, détection des fraudes
- gestion des droits numériques (DRM), sauvegarde des licences
- DRM (gestion des droits numériques), sauvegarde des licences
- gestion des droits numériques (DRM), restauration des licences
- DRM (gestion des droits numériques), restauration des licences
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- gestion des droits numériques (DRM), fonctionnalité de restauration de sauvegarde
- DRM (gestion des droits numériques), fonctionnalité de restauration de sauvegarde
- gestion des droits numériques (DRM), service de gestion de licences
- DRM (gestion des droits numériques), service de gestion des licences
- gestion des droits numériques (DRM), détection des fraudes
- DRM (gestion des droits numériques), détection des fraudes
- sauvegarde des licences DRM
- restauration des licences DRM
- licences, DRM
- licences, sauvegarde de DRM
- licences, restauration de DRM
- Fonctionnalité de restauration de sauvegarde
- Service de gestion des licences
- détection des fraudes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7718f03170077f7db624f8a99b8262239a79ca9
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104316650"
---
# <a name="backing-up-and-restoring-of-drm-licenses"></a><span data-ttu-id="6a050-130">Sauvegarde et restauration de licences DRM</span><span class="sxs-lookup"><span data-stu-id="6a050-130">Backing Up and Restoring of DRM Licenses</span></span>

<span data-ttu-id="6a050-131">Avec la fonction de restauration de sauvegarde, les utilisateurs peuvent sauvegarder et restaurer des [*licences*](wmformat-glossary.md) sur le même ordinateur ou sur d’autres ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="6a050-131">With the Backup Restore feature, users can back up and restore [*licenses*](wmformat-glossary.md) to the same computer or to other computers.</span></span> <span data-ttu-id="6a050-132">Cette fonctionnalité permet aux utilisateurs de transférer des licences vers un nouvel ordinateur ou de les replacer sur le même ordinateur (après avoir reformatage du disque dur, par exemple).</span><span class="sxs-lookup"><span data-stu-id="6a050-132">This feature enables users to transfer licenses to a new computer or back to the same computer (after reformatting the hard disk, for example).</span></span> <span data-ttu-id="6a050-133">En outre, les utilisateurs peuvent lire des fichiers ASF protégés sur plusieurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="6a050-133">In addition, users can play protected ASF files on more than one computer.</span></span>

<span data-ttu-id="6a050-134">Pour encourager l’utilisation légitime d’une licence, une stratégie de détection des fraudes restreint le nombre de fois qu’une licence peut être restaurée.</span><span class="sxs-lookup"><span data-stu-id="6a050-134">To encourage legitimate use of a license, a fraud detection policy restricts the number of times a license can be restored.</span></span> <span data-ttu-id="6a050-135">Microsoft fournit un service qui effectue le suivi du nombre d’ordinateurs sur lesquels une licence a été restaurée. Si une limite est atteinte, l’utilisateur ne peut pas restaurer la licence.</span><span class="sxs-lookup"><span data-stu-id="6a050-135">Microsoft provides a service that tracks the number of computers to which a license has been restored; if a limit is reached, the user cannot restore the license.</span></span>

## <a name="allowing-or-disallowing-the-right-to-back-up-and-restore"></a><span data-ttu-id="6a050-136">Autoriser ou non le droit de sauvegarder et de restaurer</span><span class="sxs-lookup"><span data-stu-id="6a050-136">Allowing or Disallowing the Right to Back Up and Restore</span></span>

<span data-ttu-id="6a050-137">La fonction de restauration de sauvegarde fonctionne uniquement pour les licences pour lesquelles le droit de sauvegarde et de restauration est donné.</span><span class="sxs-lookup"><span data-stu-id="6a050-137">The Backup Restore feature works only for licenses for which the Backup and Restore right is given.</span></span> <span data-ttu-id="6a050-138">Si les propriétaires de contenu ou les émetteurs de licence ne souhaitent pas cette fonctionnalité, ou s’ils émettent des licences qui contiennent un état sécurisé (par exemple, des opérations comptées ou une durée limitée), ils peuvent interdire ce droit.</span><span class="sxs-lookup"><span data-stu-id="6a050-138">If content owners or license issuers do not want this feature, or if they issue licenses that contain a secure state (such as counted operations or limited time), they can disallow this right.</span></span>

<span data-ttu-id="6a050-139">Quand une licence ne peut pas être restaurée parce qu’un utilisateur n’a pas le droit, un [*ID de clé*](wmformat-glossary.md) est passé à l’application.</span><span class="sxs-lookup"><span data-stu-id="6a050-139">When a license cannot be restored because a user does not have the right, a [*key ID*](wmformat-glossary.md) is passed to the application.</span></span> <span data-ttu-id="6a050-140">Au minimum, l’utilisateur doit être informé que certaines licences n’ont pas pu être sauvegardées, même si l’utilisateur ne connaît pas les licences auxquelles ce message fait référence.</span><span class="sxs-lookup"><span data-stu-id="6a050-140">At a minimum, the user should be notified that some licenses could not be backed up, although the user does not know which licenses this message refers to.</span></span> <span data-ttu-id="6a050-141">Si vous connaissez l’ID de clé pour les fichiers protégés disponibles, vous pouvez développer une solution plus robuste pour informer l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a050-141">If you know the key ID for available protected files, you can develop a more robust solution for informing the user.</span></span>

<span data-ttu-id="6a050-142">Par exemple, un joueur peut être développé pour une étiquette d’enregistrement qui fournit des chansons protégées sur Internet.</span><span class="sxs-lookup"><span data-stu-id="6a050-142">For example, a player could be developed for a record label that provides protected songs on the Internet.</span></span> <span data-ttu-id="6a050-143">Ces chansons et leurs ID de clé peuvent être suivis dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="6a050-143">These songs and their key IDs could be tracked in a database.</span></span> <span data-ttu-id="6a050-144">Si certaines licences n’ont pas pu être sauvegardées, l’application de lecteur peut utiliser l’ID de clé pour interroger la base de données afin d’obtenir le nom des chansons, puis informer l’utilisateur des chansons pour lesquelles les licences ne peuvent pas être sauvegardées.</span><span class="sxs-lookup"><span data-stu-id="6a050-144">If some licenses could not be backed up, the player application could use the key ID to query the database for the name of the songs, then inform the user for which songs the licenses cannot be backed up.</span></span> <span data-ttu-id="6a050-145">Ou bien, une bibliothèque musicale peut être créée pour chaque utilisateur localement, et l’ID de clé peut être utilisé pour récupérer des informations supplémentaires sur les licences qui n’ont pas pu être sauvegardées.</span><span class="sxs-lookup"><span data-stu-id="6a050-145">Or, a music library could be created for each user locally, and the key ID could be used to retrieve more information about which licenses could not be backed up.</span></span>

## <a name="the-license-management-service"></a><span data-ttu-id="6a050-146">Service de gestion des licences</span><span class="sxs-lookup"><span data-stu-id="6a050-146">The License Management Service</span></span>

<span data-ttu-id="6a050-147">Lorsque la fonctionnalité de restauration de la sauvegarde est implémentée, un service de gestion des licences hébergé par Microsoft gère la restauration des licences.</span><span class="sxs-lookup"><span data-stu-id="6a050-147">When the Backup Restore feature is implemented, a License Management Service that is hosted by Microsoft manages the restoration of licenses.</span></span>

<span data-ttu-id="6a050-148">Tout d’abord, les utilisateurs sauvegardent les licences dans l’application, par exemple, en choisissant une option de menu.</span><span class="sxs-lookup"><span data-stu-id="6a050-148">First, users back up licenses in the application, for example, by choosing a menu option.</span></span> <span data-ttu-id="6a050-149">Toutes les licences sur l’ordinateur sont sauvegardées à un emplacement spécifié, par exemple une disquette.</span><span class="sxs-lookup"><span data-stu-id="6a050-149">All licenses on the computer are backed up to a specified location, such as a floppy disk.</span></span> <span data-ttu-id="6a050-150">Ensuite, les utilisateurs restaurent les licences à l’aide de l’application, par exemple, en choisissant une option de menu et en spécifiant leur emplacement de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="6a050-150">Then, users restore licenses by using the application, for example, by choosing a menu option and specifying their backup location.</span></span>

<span data-ttu-id="6a050-151">À ce stade, l’utilisateur doit être connecté à Internet ; une demande de l’application est envoyée au service de gestion des licences.</span><span class="sxs-lookup"><span data-stu-id="6a050-151">At this point, the user must be connected to the Internet; a request from the application is sent to the License Management Service.</span></span> <span data-ttu-id="6a050-152">Si l’ordinateur à partir duquel la licence a été sauvegardée est différent de l’ordinateur d’origine (ou si l’ordinateur d’origine a été reformaté), le service de gestion des licences émet une nouvelle licence sur le nouvel ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6a050-152">If the computer from which the license was backed up is different from the original computer (or the original computer has been reformatted), the License Management Service issues a new license to the new computer.</span></span> <span data-ttu-id="6a050-153">Dans le cas contraire, la licence précédemment émise pour cet ordinateur est réémise.</span><span class="sxs-lookup"><span data-stu-id="6a050-153">Otherwise, the license that was previously issued to that computer is reissued.</span></span>

<span data-ttu-id="6a050-154">Étant donné que le service de gestion des licences récupère les informations de l’utilisateur, vous devez afficher la politique de confidentialité de Microsoft ou fournir un lien vers cette page sur le [site Web de Microsoft](https://www.microsoft.com/licensing/default).</span><span class="sxs-lookup"><span data-stu-id="6a050-154">Because the License Management Service retrieves information from the user, you must display the Microsoft privacy policy or provide a link to that page at the [Microsoft Web site](https://www.microsoft.com/licensing/default).</span></span>

> [!Note]  
> <span data-ttu-id="6a050-155">Lorsqu’un utilisateur final restaure une licence sur un autre ordinateur et que la licence requiert une individualisation, l’utilisateur final doit autoriser les composants DRM à être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="6a050-155">When an end user restores a license to a different computer and the license requires individualization, the end user must authorize the DRM components to be updated.</span></span> <span data-ttu-id="6a050-156">Vous devez implémenter un processus dans votre application de lecteur pour prendre en charge cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="6a050-156">You must implement a process in your player application to support this feature.</span></span>

 

## <a name="detecting-fraud"></a><span data-ttu-id="6a050-157">Détection des fraudes</span><span class="sxs-lookup"><span data-stu-id="6a050-157">Detecting Fraud</span></span>

<span data-ttu-id="6a050-158">L’utilisateur est autorisé à restaurer une licence un nombre limité de fois.</span><span class="sxs-lookup"><span data-stu-id="6a050-158">The user is allowed to restore a license a limited number of times.</span></span> <span data-ttu-id="6a050-159">Chaque fois qu’une licence est restaurée, le service de gestion des licences la suit et incrémente le nombre de cette licence d’une unité.</span><span class="sxs-lookup"><span data-stu-id="6a050-159">Each time a license is restored, the License Management Service tracks it and increments the count for that license by one.</span></span> <span data-ttu-id="6a050-160">Lors de la restauration d’une licence sur un ordinateur sur lequel la licence a été restaurée précédemment (par exemple, l’ordinateur à partir duquel la licence a été sauvegardée), le nombre n’est pas augmenté.</span><span class="sxs-lookup"><span data-stu-id="6a050-160">When restoring a license to a computer to which the license has been restored previously (for example, the computer from which the license was backed up), the count is not increased.</span></span> <span data-ttu-id="6a050-161">Un ordinateur est considéré comme différent s’il dispose d’un nouveau système d’exploitation ou si le système d’exploitation a été réinstallé.</span><span class="sxs-lookup"><span data-stu-id="6a050-161">A computer is considered to be different if it has a new operating system, or the operating system has been re-installed.</span></span>

<span data-ttu-id="6a050-162">Conformément à la stratégie de détection des fraudes de Microsoft, lorsqu’une licence a été restaurée un certain nombre de fois, l’application reçoit une URL à partir des composants DRM et est chargée d’ouvrir un navigateur et d’afficher la page Web, ce qui indique que le contrat de licence n’a peut-être pas été respecté.</span><span class="sxs-lookup"><span data-stu-id="6a050-162">In accordance with Microsoft's fraud detection policy, when a license has been restored a certain number of times, the application receives a URL from the DRM components and is responsible for opening a browser and displaying the Web page, which indicates that the license agreement might have been violated.</span></span> <span data-ttu-id="6a050-163">L’utilisateur doit contacter le distributeur de licences, qui doit ensuite déterminer si la demande est valide.</span><span class="sxs-lookup"><span data-stu-id="6a050-163">The user must contact the license distributor, who must then determine whether the request is valid.</span></span>

> [!Note]  
> <span data-ttu-id="6a050-164">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="6a050-164">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6a050-165">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a050-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a050-166">**Fonctionnalités de Rights Management numérique**</span><span class="sxs-lookup"><span data-stu-id="6a050-166">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="6a050-167">**Sauvegarde et restauration de licences**</span><span class="sxs-lookup"><span data-stu-id="6a050-167">**Backing Up and Restoring Licenses**</span></span>](backing-up-and-restoring-licenses.md)
</dt> </dl>

 

 




