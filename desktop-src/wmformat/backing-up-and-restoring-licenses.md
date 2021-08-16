---
title: Sauvegarde et restauration de licences
description: Sauvegarde et restauration de licences
ms.assetid: 59be02fe-f207-4161-8765-9a88a8050248
keywords:
- Windows Media Format SDK, sauvegarde des licences
- Windows Media Format SDK, restauration de licences
- Windows Media Format SDK, sauvegarde et restauration de licence
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
ms.openlocfilehash: 378a41d975e8f19d38c637d585759d0038f5b86550769ae49d6a6490844f223e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028137"
---
# <a name="backing-up-and-restoring-licenses"></a>Sauvegarde et restauration de licences

Les processus de sauvegarde et de restauration sont asynchrones. Ils sont déclenchés lorsque l’utilisateur sélectionne une commande de menu ou une option dans l’application pour sauvegarder ou restaurer des licences. Vous devez autoriser l’utilisateur à spécifier les emplacements à partir desquels les licences doivent être sauvegardées et restaurées.

Pour sauvegarder des licences :

1.  Utilisez la fonction [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) pour créer l’objet de restauration de sauvegarde.
2.  Appelez la méthode [**IWMBackupRestoreProps :: échec SetProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) pour définir le chemin de sauvegarde (l’emplacement où vous allez écrire les fichiers, par exemple A : \\ ou D : \\ licences).
3.  Appelez la méthode [**IWMLicenseBackup :: BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) pour sauvegarder les licences dans le chemin d’accès spécifié.

Les événements suivants sont envoyés à la méthode [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) :

-   **WMT \_ BACKUPRESTORE \_ Begin** indique que le processus de sauvegarde a démarré.
-   **WMT \_ BACKUPRESTORE \_ end** indique que le processus de sauvegarde est terminé.
-   **WMT \_ \_Licence restreinte** indique qu’une ou plusieurs licences ne peuvent pas être sauvegardées parce que le droit a été interdit par le propriétaire du contenu.

L’ID de clé est également inclus dans ce message. Si vous avez implémenté une base de données pour les fichiers protégés qui comprend l’ID de clé et les métadonnées, vous pouvez afficher un message à l’utilisateur avec le titre spécifique (par exemple, un titre de chanson) pour lequel la licence ne peut pas être sauvegardée. Dans le cas contraire, le message doit être générique et informer l’utilisateur que certaines licences ne peuvent pas être sauvegardées.

Pour restaurer les licences :

1.  Utilisez la fonction **WMCreateBackupRestorer** pour créer l’objet de restauration de sauvegarde.
2.  Appelez la méthode **IWMBackupRestoreProps :: échec SetProp** pour définir le chemin d’accès de restauration à l’emplacement où les licences sont sauvegardées.
3.  Appelez la méthode [**IWMLicenseRestore :: RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) pour restaurer les licences à partir de cet emplacement.

Les événements suivants sont envoyés à la méthode [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) :

-   **WMT \_ BACKUPRESTORE la \_ connexion** indique que l’application se connecte au service de gestion des licences.
-   **WMT \_ La \_ déconnexion de BACKUPRESTORE** indique que l’application est déconnectée du service de gestion des licences.
-   **WMT \_ BACKUPRESTORE \_ Begin** indique que le processus de restauration a démarré.
-   **WMT \_ BACKUPRESTORE \_ end** indique que le processus de restauration est terminé.

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités de Rights Management numérique**](digital-rights-management-features.md)
</dt> <dt>

[**Interface IWMBackupRestoreProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops)
</dt> <dt>

[**Interface IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)
</dt> <dt>

[**Interface IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)
</dt> </dl>

 

 




