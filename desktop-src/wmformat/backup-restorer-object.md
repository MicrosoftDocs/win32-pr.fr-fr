---
title: Objet de restauration de sauvegarde
description: Objet de restauration de sauvegarde
ms.assetid: 83ce28c0-fd17-46ff-94c0-d28124a0e56a
keywords:
- Windows Media Format SDK, objets du remagasin de sauvegarde
- ASF (Advanced Systems Format), objets de restauration de sauvegarde
- ASF (format des systèmes avancés), objets du remagasin de sauvegarde
- objets, objets de restauration de sauvegarde
- restauration de sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d08e8bec9bb7bbc2a45fbf632e69d230a2536633
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106512716"
---
# <a name="backup-restorer-object"></a>Objet de restauration de sauvegarde

Le remagasin de sauvegarde fournit des interfaces pour gérer la sauvegarde des licences, généralement sur des supports amovibles, puis pour la restauration de ces licences sur un nouvel ordinateur.

L’objet de restauration de sauvegarde est créé par la fonction [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) , qui définit un pointeur vers une interface [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) . Les autres interfaces de l’objet de restauration de sauvegarde peuvent être obtenues en appelant la méthode **QueryInterface** .

Les interfaces suivantes sont prises en charge par l’objet de restauration de sauvegarde.



| Interface                                              | Description                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMBackupRestoreProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | Définit et récupère les propriétés requises par les interfaces [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) et [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) . |
| [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | Sauvegarde les licences, en général afin qu’elles puissent être restaurées sur un autre ordinateur.                                                                          |
| [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | Restaure les licences.                                                                                                                                        |



 

L’interface de rappel suivante doit être implémentée par l’application afin d’utiliser l’objet de restauration de sauvegarde.



| Interface                                      | Description                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Reçoit des messages d’état des processus qui s’exécutent dans un thread séparé. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Sauvegarde et restauration de licences**](backing-up-and-restoring-licenses.md)
</dt> <dt>

[**Objets**](objects.md)
</dt> </dl>

 

 




