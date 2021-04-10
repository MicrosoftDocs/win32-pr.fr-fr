---
description: Modèle d’objet VDS
ms.assetid: e5fcc19a-e170-4918-85eb-c1457776795a
title: Modèle d’objet VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae998955c5d0b7834cf4d88b901537f3644a2ab
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104211150"
---
# <a name="vds-object-model"></a><span data-ttu-id="e6f33-103">Modèle d’objet VDS</span><span class="sxs-lookup"><span data-stu-id="e6f33-103">VDS Object Model</span></span>

<span data-ttu-id="e6f33-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e6f33-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="e6f33-105">VDS fournit un accès indirect aux dispositifs de stockage basés sur l’hôte, tels que les disques et les lecteurs de CD-ROM, et aux baies de disques qui sont gérées par les contrôleurs RAID matériels.</span><span class="sxs-lookup"><span data-stu-id="e6f33-105">VDS provides indirect access to host-based storage devices, such as disks and CD-ROM devices, and to disk arrays that are managed by hardware RAID controllers.</span></span> <span data-ttu-id="e6f33-106">Tandis que certaines entités de stockage modélisent des appareils physiques, d’autres modélisent des constructions virtuelles : des volumes, des partitions, etc.</span><span class="sxs-lookup"><span data-stu-id="e6f33-106">While some storage entities model physical devices, others model virtual constructs: volumes, partitions, and so on.</span></span> <span data-ttu-id="e6f33-107">Les objets qui sont décrits dans cette rubrique représentent les entités physiques et virtuelles de VDS.</span><span class="sxs-lookup"><span data-stu-id="e6f33-107">The objects that are described in this topic represent both the physical and virtual entities of VDS.</span></span>

<span data-ttu-id="e6f33-108">Les applications appellent les méthodes exposées par ces objets et VDS appellent le fournisseur approprié pour effectuer les opérations de stockage demandées.</span><span class="sxs-lookup"><span data-stu-id="e6f33-108">Applications call the methods that are exposed by these objects and VDS calls the appropriate provider to perform the requested storage operations.</span></span> <span data-ttu-id="e6f33-109">Une application n’appelle jamais directement un programme fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e6f33-109">An application never calls a provider program directly.</span></span>

### <a name="classification-of-objects"></a><span data-ttu-id="e6f33-110">Classification des objets</span><span class="sxs-lookup"><span data-stu-id="e6f33-110">Classification of Objects</span></span>

<span data-ttu-id="e6f33-111">Comme le montre l’illustration suivante, les programmes de fournisseur de logiciels implémentent des objets qui modélisent des entités basées sur l’hôte. les programmes de fournisseur de matériel implémentent des objets qui modélisent des appareils RAID matériels internes et externes. les objets communs restants sont indépendants du fournisseur ou mis en œuvre par VDS.</span><span class="sxs-lookup"><span data-stu-id="e6f33-111">As the following illustration shows, software provider programs implement objects that model host-based entities; hardware provider programs implement objects that model internal and external hardware RAID devices; the remaining common objects are either provider-independent, or are implemented by VDS.</span></span> <span data-ttu-id="e6f33-112">Une broche, qui n’est pas un objet VDS, est un terme de support de stockage générique qui se compose d’étendues de disque ou de lecteur.</span><span class="sxs-lookup"><span data-stu-id="e6f33-112">A spindle, which is not a VDS object, is a term for generic storage media that comprises of disk or drive extents.</span></span>

![Diagramme qui montre une classification d’objets, définie comme « objets communs », « objets de fournisseur de logiciels » et « objets de fournisseur de matériel ».](images/vdsobjectmodel.png)

<span data-ttu-id="e6f33-114">Pour en savoir plus sur le comportement de chaque objet, sélectionnez l’une des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="e6f33-114">To learn more about the behavior of each object, select from the following topics:</span></span>

-   <span data-ttu-id="e6f33-115">Le chargeur de service et les objets de service, consultez [démarrage et objets de service](startup-and-service-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e6f33-115">Service loader and service objects, see [Startup and Service Objects](startup-and-service-objects.md).</span></span>
-   <span data-ttu-id="e6f33-116">Les objets d’énumération et Async, consultez la page [objets d’assistance](helper-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e6f33-116">Enumeration and async objects, see [Helper Objects](helper-objects.md).</span></span>
-   <span data-ttu-id="e6f33-117">Fournisseur, consultez l' [objet Provider](provider-object.md).</span><span class="sxs-lookup"><span data-stu-id="e6f33-117">Provider object, see [Provider Object](provider-object.md).</span></span>
-   <span data-ttu-id="e6f33-118">Les objets Pack, disque, volume et Plex volume, consultez [objets fournisseur de logiciels](software-provider-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e6f33-118">Pack, disk, volume, and volume plex objects, see [Software Provider Objects](software-provider-objects.md).</span></span>
-   <span data-ttu-id="e6f33-119">Les objets de sous-système, de contrôleur, de lecteur, de LUN et de plex LUN, consultez la rubrique [objets de fournisseur de matériel](hardware-provider-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e6f33-119">Subsystem, controller, drive, LUN, and LUN plex objects, see [Hardware Provider Objects](hardware-provider-objects.md).</span></span>

### <a name="object-creation"></a><span data-ttu-id="e6f33-120">Création d’objets</span><span class="sxs-lookup"><span data-stu-id="e6f33-120">Object Creation</span></span>

<span data-ttu-id="e6f33-121">Les opérations de configuration et de requête associées à la création d’objets peuvent prendre beaucoup de temps. par conséquent, VDS appelle toutes les méthodes de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e6f33-121">The configuration and query operations that are associated with object creation can take considerable time to complete; as such, VDS invokes all methods asynchronously.</span></span> <span data-ttu-id="e6f33-122">Le fournisseur de découverte retourne tous les événements de modification d’État, d’erreur ou d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="e6f33-122">The discovering provider returns all completion, error, or state change events.</span></span> <span data-ttu-id="e6f33-123">Les fournisseurs de logiciels journalisent également toutes les erreurs et les modifications d’État importantes.</span><span class="sxs-lookup"><span data-stu-id="e6f33-123">Software providers also log all the errors and significant state changes.</span></span>

### <a name="object-deletion"></a><span data-ttu-id="e6f33-124">Suppression de l'objet</span><span class="sxs-lookup"><span data-stu-id="e6f33-124">Object Deletion</span></span>

<span data-ttu-id="e6f33-125">Plusieurs méthodes VDS suppriment ou transforment des objets VDS.</span><span class="sxs-lookup"><span data-stu-id="e6f33-125">Several VDS methods delete or transform VDS objects.</span></span> <span data-ttu-id="e6f33-126">Un appelant peut conserver une référence, au moyen d’un pointeur d’interface, à un objet supprimé après le retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="e6f33-126">A caller can hold a reference, by way of an interface pointer, to a deleted object after the method returns.</span></span> <span data-ttu-id="e6f33-127">Lorsque l’appelant libère l’interface, VDS supprime l’objet.</span><span class="sxs-lookup"><span data-stu-id="e6f33-127">When the caller releases the interface, VDS deletes the object.</span></span>

<span data-ttu-id="e6f33-128">En ce qui concerne la suppression d’objets, les appelants doivent s’abstenir d’appeler tout, à l’exception de la méthode [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="e6f33-128">With regard to object deletion, callers should refrain from invoking anything except the [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on these interfaces.</span></span> <span data-ttu-id="e6f33-129">Le fournisseur doit être suffisamment robuste pour traiter les appelants errants ; Si un appelant appelle une méthode sur un objet supprimé, le fournisseur doit retourner l' **\_ objet VDS \_ E \_ Deleted**.</span><span class="sxs-lookup"><span data-stu-id="e6f33-129">The provider must be robust enough to deal with errant callers; if a caller invokes a method on a deleted object, the provider should return **VDS\_E\_OBJECT\_DELETED**.</span></span>

### <a name="service-initialization"></a><span data-ttu-id="e6f33-130">Initialisation du service</span><span class="sxs-lookup"><span data-stu-id="e6f33-130">Service Initialization</span></span>

<span data-ttu-id="e6f33-131">VDS fournit un identificateur de classe (CLSID) pour le chargeur de service et les objets de service, mais seul le CLSID du chargeur de service est public.</span><span class="sxs-lookup"><span data-stu-id="e6f33-131">VDS supplies a class identifier (Clsid) for the service loader and the service objects, but only the service loader Clsid is public.</span></span> <span data-ttu-id="e6f33-132">L’initialisation du service se produit lorsque les fournisseurs, une application appelante et le service effectuent les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="e6f33-132">Service initialization occurs when the providers, a calling application, and the service perform the following tasks:</span></span>

-   <span data-ttu-id="e6f33-133">Chaque nouveau fournisseur appelle la méthode [**IVdsAdmin :: RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) au cours de l’installation pour s’inscrire auprès de VDS.</span><span class="sxs-lookup"><span data-stu-id="e6f33-133">Each new provider invokes the [**IVdsAdmin::RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) method during installation to register with VDS.</span></span> <span data-ttu-id="e6f33-134">L’appel crée une clé de Registre sous la ruche système, identifiée par le GUID d’objet du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e6f33-134">The call creates a registry key under the SYSTEM hive, identified by the object GUID of the provider.</span></span> <span data-ttu-id="e6f33-135">Contenu sous cette clé est le CLSID de l’objet fournisseur, le nom, la version et le GUID de la version du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e6f33-135">Contained under this key is the Clsid of the provider object, the name, version, and the version GUID of the provider.</span></span>
    > [!Note]  
    > <span data-ttu-id="e6f33-136">Les GUID d’objet de fournisseur sont persistants ; les GUID d’objet logiciels et matériels ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="e6f33-136">Provider object GUIDs are persistent; software and hardware object GUIDs are not.</span></span>

     

-   <span data-ttu-id="e6f33-137">Une application appelle la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , en passant le CLSID du chargeur de service comme argument.</span><span class="sxs-lookup"><span data-stu-id="e6f33-137">An application calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function, passing the service loader Clsid as an argument.</span></span> <span data-ttu-id="e6f33-138">Avec un pointeur vers l’objet service Loader, l’application peut démarrer VDS localement ou à distance en transmettant le nom d’ordinateur souhaité en tant que paramètre à la méthode [**IVdsServiceLoader :: LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) .</span><span class="sxs-lookup"><span data-stu-id="e6f33-138">With a pointer to the service loader object, the application can start VDS either locally or remotely by passing the desired computer name as a parameter to the [**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) method.</span></span>
-   <span data-ttu-id="e6f33-139">Lorsque l’application initiale est attachée au service, VDS appelle d’abord [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) sur chaque CLSID trouvé sous la clé de Registre, puis appelle la méthode [**IVdsProviderPrivate :: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) sur chaque fournisseur pour initialiser les programmes.</span><span class="sxs-lookup"><span data-stu-id="e6f33-139">When the initial application attaches to the service, VDS first calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on each Clsid found under the registry key, and then calls the [**IVdsProviderPrivate::OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) method on each provider to initialize the programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6f33-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e6f33-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6f33-141">À propos de VDS</span><span class="sxs-lookup"><span data-stu-id="e6f33-141">About VDS</span></span>](about-vds.md)
</dt> <dt>

[<span data-ttu-id="e6f33-142">**IVdsAdmin :: RegisterProvider**</span><span class="sxs-lookup"><span data-stu-id="e6f33-142">**IVdsAdmin::RegisterProvider**</span></span>](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider)
</dt> <dt>

[<span data-ttu-id="e6f33-143">**IVdsServiceLoader::LoadService**</span><span class="sxs-lookup"><span data-stu-id="e6f33-143">**IVdsServiceLoader::LoadService**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[<span data-ttu-id="e6f33-144">**IVdsProviderPrivate :: OnLoad**</span><span class="sxs-lookup"><span data-stu-id="e6f33-144">**IVdsProviderPrivate::OnLoad**</span></span>](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> </dl>

 

 
