---
title: Sauvegarde et restauration de licences
description: Sauvegarde et restauration de licences
ms.assetid: 59be02fe-f207-4161-8765-9a88a8050248
keywords:
- Windows Media Format SDK, sauvegarde des licences
- Windows Media Format SDK, restauration de licences
- Windows Media Format SDK, sauvegarde et restauration de licences
- ASF (Advanced Systems Format), sauvegarde des licences
- ASF (format des systèmes avancés), sauvegarde des licences
- ASF (Advanced Systems Format), restauration des licences
- ASF (format avancé des systèmes), restauration des licences
- ASF (Advanced Systems Format), sauvegarde et restauration de la licence
- ASF (format avancé des systèmes), sauvegarde et restauration de la licence
- gestion des droits numériques (DRM), sauvegarde des licences
- DRM (gestion des droits numériques), sauvegarde des licences
- gestion des droits numériques (DRM), restauration des licences
- DRM (gestion des droits numériques), restauration des licences
- gestion des droits numériques (DRM), sauvegarde et restauration de la licence
- DRM (gestion des droits numériques), sauvegarde et restauration de la licence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10d8e76c191225288a1021e08e4c77e7e14f3c6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723530"
---
# <a name="backing-up-and-restoring-licenses"></a><span data-ttu-id="7b57e-118">Sauvegarde et restauration de licences</span><span class="sxs-lookup"><span data-stu-id="7b57e-118">Backing Up and Restoring Licenses</span></span>

<span data-ttu-id="7b57e-119">Les processus de sauvegarde et de restauration sont asynchrones.</span><span class="sxs-lookup"><span data-stu-id="7b57e-119">The backup and restore processes are asynchronous.</span></span> <span data-ttu-id="7b57e-120">Ils sont déclenchés lorsque l’utilisateur sélectionne une commande de menu ou une option dans l’application pour sauvegarder ou restaurer des licences.</span><span class="sxs-lookup"><span data-stu-id="7b57e-120">They are triggered when the user selects a menu command or option in the application to back up or restore licenses.</span></span> <span data-ttu-id="7b57e-121">Vous devez autoriser l’utilisateur à spécifier les emplacements à partir desquels les licences doivent être sauvegardées et restaurées.</span><span class="sxs-lookup"><span data-stu-id="7b57e-121">You should allow the user to specify the locations where licenses must be backed up to and restored from.</span></span>

<span data-ttu-id="7b57e-122">Pour sauvegarder des licences :</span><span class="sxs-lookup"><span data-stu-id="7b57e-122">To back up licenses:</span></span>

1.  <span data-ttu-id="7b57e-123">Utilisez la fonction [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) pour créer l’objet de restauration de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="7b57e-123">Use the [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) function to create the backup restorer object.</span></span>
2.  <span data-ttu-id="7b57e-124">Appelez la méthode [**IWMBackupRestoreProps :: échec SetProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) pour définir le chemin de sauvegarde (l’emplacement où vous allez écrire les fichiers, par exemple A : \\ ou D : \\ licences).</span><span class="sxs-lookup"><span data-stu-id="7b57e-124">Call the [**IWMBackupRestoreProps::SetProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) method to set the backup path (the location where you will write the files, such as A:\\ or D:\\Licenses).</span></span>
3.  <span data-ttu-id="7b57e-125">Appelez la méthode [**IWMLicenseBackup :: BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) pour sauvegarder les licences dans le chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="7b57e-125">Call the [**IWMLicenseBackup::BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) method to back up the licenses to the specified path.</span></span>

<span data-ttu-id="7b57e-126">Les événements suivants sont envoyés à la méthode [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) :</span><span class="sxs-lookup"><span data-stu-id="7b57e-126">The following events are sent to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method:</span></span>

-   <span data-ttu-id="7b57e-127">**WMT \_ BACKUPRESTORE \_ Begin** indique que le processus de sauvegarde a démarré.</span><span class="sxs-lookup"><span data-stu-id="7b57e-127">**WMT\_BACKUPRESTORE\_BEGIN** indicates the backup process has started.</span></span>
-   <span data-ttu-id="7b57e-128">**WMT \_ BACKUPRESTORE \_ end** indique que le processus de sauvegarde est terminé.</span><span class="sxs-lookup"><span data-stu-id="7b57e-128">**WMT\_BACKUPRESTORE\_END** indicates the backup process has been completed.</span></span>
-   <span data-ttu-id="7b57e-129">**WMT \_ \_Licence restreinte** indique qu’une ou plusieurs licences ne peuvent pas être sauvegardées parce que le droit a été interdit par le propriétaire du contenu.</span><span class="sxs-lookup"><span data-stu-id="7b57e-129">**WMT\_RESTRICTED\_LICENSE** indicates that one or more licenses cannot be backed up because the right has been disallowed by the content owner.</span></span>

<span data-ttu-id="7b57e-130">L’ID de clé est également inclus dans ce message.</span><span class="sxs-lookup"><span data-stu-id="7b57e-130">The key ID is also included in this message.</span></span> <span data-ttu-id="7b57e-131">Si vous avez implémenté une base de données pour les fichiers protégés qui comprend l’ID de clé et les métadonnées, vous pouvez afficher un message à l’utilisateur avec le titre spécifique (par exemple, un titre de chanson) pour lequel la licence ne peut pas être sauvegardée.</span><span class="sxs-lookup"><span data-stu-id="7b57e-131">If you have implemented a database for protected files that includes the key ID and metadata, you can display a message to the user with the specific title (such as a song title) for which the license cannot be backed up.</span></span> <span data-ttu-id="7b57e-132">Dans le cas contraire, le message doit être générique et informer l’utilisateur que certaines licences ne peuvent pas être sauvegardées.</span><span class="sxs-lookup"><span data-stu-id="7b57e-132">Otherwise, the message must be generic and inform the user that some licenses cannot be backed up.</span></span>

<span data-ttu-id="7b57e-133">Pour restaurer les licences :</span><span class="sxs-lookup"><span data-stu-id="7b57e-133">To restore licenses:</span></span>

1.  <span data-ttu-id="7b57e-134">Utilisez la fonction **WMCreateBackupRestorer** pour créer l’objet de restauration de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="7b57e-134">Use the **WMCreateBackupRestorer** function to create the backup restorer object.</span></span>
2.  <span data-ttu-id="7b57e-135">Appelez la méthode **IWMBackupRestoreProps :: échec SetProp** pour définir le chemin d’accès de restauration à l’emplacement où les licences sont sauvegardées.</span><span class="sxs-lookup"><span data-stu-id="7b57e-135">Call the **IWMBackupRestoreProps::SetProp** method to set the restore path to the location where licenses are backed up.</span></span>
3.  <span data-ttu-id="7b57e-136">Appelez la méthode [**IWMLicenseRestore :: RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) pour restaurer les licences à partir de cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="7b57e-136">Call the [**IWMLicenseRestore::RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) method to restore licenses from that location.</span></span>

<span data-ttu-id="7b57e-137">Les événements suivants sont envoyés à la méthode [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) :</span><span class="sxs-lookup"><span data-stu-id="7b57e-137">The following events are sent to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method:</span></span>

-   <span data-ttu-id="7b57e-138">**WMT \_ BACKUPRESTORE la \_ connexion** indique que l’application se connecte au service de gestion des licences.</span><span class="sxs-lookup"><span data-stu-id="7b57e-138">**WMT\_BACKUPRESTORE\_CONNECTING** indicates that the application is connecting to the License Management Service.</span></span>
-   <span data-ttu-id="7b57e-139">**WMT \_ La \_ déconnexion de BACKUPRESTORE** indique que l’application est déconnectée du service de gestion des licences.</span><span class="sxs-lookup"><span data-stu-id="7b57e-139">**WMT\_BACKUPRESTORE\_DISCONNECTING** indicates that the application is disconnecting from the License Management Service.</span></span>
-   <span data-ttu-id="7b57e-140">**WMT \_ BACKUPRESTORE \_ Begin** indique que le processus de restauration a démarré.</span><span class="sxs-lookup"><span data-stu-id="7b57e-140">**WMT\_BACKUPRESTORE\_BEGIN** indicates the restore process has started.</span></span>
-   <span data-ttu-id="7b57e-141">**WMT \_ BACKUPRESTORE \_ end** indique que le processus de restauration est terminé.</span><span class="sxs-lookup"><span data-stu-id="7b57e-141">**WMT\_BACKUPRESTORE\_END** indicates the restore process has been completed.</span></span>

> [!Note]  
> <span data-ttu-id="7b57e-142">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="7b57e-142">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7b57e-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b57e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b57e-144">**Fonctionnalités de Rights Management numérique**</span><span class="sxs-lookup"><span data-stu-id="7b57e-144">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="7b57e-145">**Interface IWMBackupRestoreProps**</span><span class="sxs-lookup"><span data-stu-id="7b57e-145">**IWMBackupRestoreProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops)
</dt> <dt>

[<span data-ttu-id="7b57e-146">**Interface IWMLicenseBackup**</span><span class="sxs-lookup"><span data-stu-id="7b57e-146">**IWMLicenseBackup Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)
</dt> <dt>

[<span data-ttu-id="7b57e-147">**Interface IWMLicenseRestore**</span><span class="sxs-lookup"><span data-stu-id="7b57e-147">**IWMLicenseRestore Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)
</dt> </dl>

 

 




