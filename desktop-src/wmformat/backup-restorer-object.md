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
# <a name="backup-restorer-object"></a><span data-ttu-id="83e75-108">Objet de restauration de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="83e75-108">Backup Restorer Object</span></span>

<span data-ttu-id="83e75-109">Le remagasin de sauvegarde fournit des interfaces pour gérer la sauvegarde des licences, généralement sur des supports amovibles, puis pour la restauration de ces licences sur un nouvel ordinateur.</span><span class="sxs-lookup"><span data-stu-id="83e75-109">The backup restorer provides interfaces to handle backing up licenses, typically onto removable media, and then restoring those licenses onto a new computer.</span></span>

<span data-ttu-id="83e75-110">L’objet de restauration de sauvegarde est créé par la fonction [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) , qui définit un pointeur vers une interface [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) .</span><span class="sxs-lookup"><span data-stu-id="83e75-110">The backup restorer object is created by the [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) function, which sets a pointer to an [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) interface.</span></span> <span data-ttu-id="83e75-111">Les autres interfaces de l’objet de restauration de sauvegarde peuvent être obtenues en appelant la méthode **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="83e75-111">The other interfaces of the backup restorer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="83e75-112">Les interfaces suivantes sont prises en charge par l’objet de restauration de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="83e75-112">The following interfaces are supported by the backup restorer object.</span></span>



| <span data-ttu-id="83e75-113">Interface</span><span class="sxs-lookup"><span data-stu-id="83e75-113">Interface</span></span>                                              | <span data-ttu-id="83e75-114">Description</span><span class="sxs-lookup"><span data-stu-id="83e75-114">Description</span></span>                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83e75-115">**IWMBackupRestoreProps**</span><span class="sxs-lookup"><span data-stu-id="83e75-115">**IWMBackupRestoreProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | <span data-ttu-id="83e75-116">Définit et récupère les propriétés requises par les interfaces [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) et [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) .</span><span class="sxs-lookup"><span data-stu-id="83e75-116">Sets and retrieves properties required by the [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) and [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) interfaces.</span></span> |
| [<span data-ttu-id="83e75-117">**IWMLicenseBackup**</span><span class="sxs-lookup"><span data-stu-id="83e75-117">**IWMLicenseBackup**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | <span data-ttu-id="83e75-118">Sauvegarde les licences, en général afin qu’elles puissent être restaurées sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="83e75-118">Backs up licenses, typically so that they can be restored onto another computer.</span></span>                                                                          |
| [<span data-ttu-id="83e75-119">**IWMLicenseRestore**</span><span class="sxs-lookup"><span data-stu-id="83e75-119">**IWMLicenseRestore**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | <span data-ttu-id="83e75-120">Restaure les licences.</span><span class="sxs-lookup"><span data-stu-id="83e75-120">Restores licenses.</span></span>                                                                                                                                        |



 

<span data-ttu-id="83e75-121">L’interface de rappel suivante doit être implémentée par l’application afin d’utiliser l’objet de restauration de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="83e75-121">The following callback interface must be implemented by the application in order to use the backup restorer object.</span></span>



| <span data-ttu-id="83e75-122">Interface</span><span class="sxs-lookup"><span data-stu-id="83e75-122">Interface</span></span>                                      | <span data-ttu-id="83e75-123">Description</span><span class="sxs-lookup"><span data-stu-id="83e75-123">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="83e75-124">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="83e75-124">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="83e75-125">Reçoit des messages d’état des processus qui s’exécutent dans un thread séparé.</span><span class="sxs-lookup"><span data-stu-id="83e75-125">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="83e75-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="83e75-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83e75-127">**Sauvegarde et restauration de licences**</span><span class="sxs-lookup"><span data-stu-id="83e75-127">**Backing Up and Restoring Licenses**</span></span>](backing-up-and-restoring-licenses.md)
</dt> <dt>

[<span data-ttu-id="83e75-128">**Objets**</span><span class="sxs-lookup"><span data-stu-id="83e75-128">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




