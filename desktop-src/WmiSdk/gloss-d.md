---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 50397050-3b5c-4683-972c-95d9f661b365
ms.tgt_platform: multiple
title: D (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d469b94ec6649c64722fb414880d2e79fc3c88b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034618"
---
# <a name="d-wmi"></a><span data-ttu-id="a411c-103">D (WMI)</span><span class="sxs-lookup"><span data-stu-id="a411c-103">D (WMI)</span></span>

<span data-ttu-id="a411c-104">[A](gloss-a.md) B [C](gloss-c.md) D [e](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="a411c-104">[A](gloss-a.md) B [C](gloss-c.md) D [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a411c-105"><span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**Date/heure**</span><span class="sxs-lookup"><span data-stu-id="a411c-105"><span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**datetime**</span></span>
</dt> <dd>

<span data-ttu-id="a411c-106">Voir [*DateTime CIM*](gloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="a411c-106">See [*CIM datetime*](gloss-c.md).</span></span>

</dd> <dt>

<span data-ttu-id="a411c-107"><span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**fournisseur découplé**</span><span class="sxs-lookup"><span data-stu-id="a411c-107"><span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**decoupled provider**</span></span>
</dt> <dd>

<span data-ttu-id="a411c-108">Fournisseur hébergé dans un processus distinct de WMI.</span><span class="sxs-lookup"><span data-stu-id="a411c-108">A provider hosted in a separate process from WMI.</span></span> <span data-ttu-id="a411c-109">Les fournisseurs découplés sont la méthode recommandée pour instrumenter une application, car le fournisseur peut contrôler sa propre durée de vie au lieu d’être lancé chaque fois qu’un utilisateur accède au fournisseur via WMI.</span><span class="sxs-lookup"><span data-stu-id="a411c-109">Decoupled providers are the recommended way to instrument an application, because the provider can control its own lifetime instead of being started each time a user accesses the provider through WMI.</span></span>

</dd> <dt>

<span data-ttu-id="a411c-110"><span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**accès direct**</span><span class="sxs-lookup"><span data-stu-id="a411c-110"><span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**direct access**</span></span>
</dt> <dd>

<span data-ttu-id="a411c-111">Méthode permettant d’accéder aux propriétés et aux méthodes fournies par WMI dans un script comme s’il s’agissait de propriétés et de méthodes Automation de [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="a411c-111">A way to access properties and methods supplied by WMI in a script as if they were automation properties and methods of [**SWbemObject**](swbemobject.md).</span></span>

<span data-ttu-id="a411c-112">Accès indirect : `VolumeName = MyDisk.Properties_("VolumeName")`</span><span class="sxs-lookup"><span data-stu-id="a411c-112">Nondirect access: `VolumeName = MyDisk.Properties_("VolumeName")`</span></span>

<span data-ttu-id="a411c-113">Accès direct : `VolumeName = MyDisk.VolumeName`</span><span class="sxs-lookup"><span data-stu-id="a411c-113">Direct access: `VolumeName = MyDisk.VolumeName`</span></span>

</dd> <dt>

<span data-ttu-id="a411c-114"><span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**DMTF (Distributed Management Task Force)**</span><span class="sxs-lookup"><span data-stu-id="a411c-114"><span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**Distributed Management Task Force (DMTF)**</span></span>
</dt> <dd>

<span data-ttu-id="a411c-115">Organisation internationale de normalisation qui collabore avec les principaux fournisseurs de technologies, y compris Microsoft, pour mener à bien le développement, l’adoption et l’unification des normes et des initiatives de gestion pour les environnements de bureau, d’entreprise et Internet.</span><span class="sxs-lookup"><span data-stu-id="a411c-115">An international standards organization that works with key technology vendors, including Microsoft, to lead the development, adoption, and unification of management standards and initiatives for desktop, enterprise, and Internet environments.</span></span>

</dd> <dt>

<span data-ttu-id="a411c-116"><span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DMTF**</span><span class="sxs-lookup"><span data-stu-id="a411c-116"><span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DMTF**</span></span>
</dt> <dd>

<span data-ttu-id="a411c-117">Voir *Distributed Management Task Force (DMTF)*.</span><span class="sxs-lookup"><span data-stu-id="a411c-117">See *Distributed Management Task Force (DMTF)*.</span></span>

</dd> <dt>

<span data-ttu-id="a411c-118"><span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**classe dynamique**</span><span class="sxs-lookup"><span data-stu-id="a411c-118"><span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**dynamic class**</span></span>
</dt> <dd>

<span data-ttu-id="a411c-119">Classe CIM dont la définition est fournie par un [*fournisseur*](gloss-p.md) au moment de l’exécution, selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="a411c-119">A CIM class whose definition is supplied by a [*provider*](gloss-p.md) at run time, as required.</span></span> <span data-ttu-id="a411c-120">Les classes dynamiques représentent des [*objets managés*](gloss-m.md) spécifiques au fournisseur et ne sont pas stockées dans le [*référentiel CIM*](gloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="a411c-120">Dynamic classes represent provider-specific [*managed objects*](gloss-m.md) and are not stored in the [*CIM repository*](gloss-c.md).</span></span> <span data-ttu-id="a411c-121">Les classes dynamiques ne prennent en charge que les *instances dynamiques*.</span><span class="sxs-lookup"><span data-stu-id="a411c-121">Dynamic classes support only *dynamic instances*.</span></span>

</dd> <dt>

<span data-ttu-id="a411c-122"><span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**instance dynamique**</span><span class="sxs-lookup"><span data-stu-id="a411c-122"><span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**dynamic instance**</span></span>
</dt> <dd>

<span data-ttu-id="a411c-123">Instance d’une classe CIM fournie par un [*fournisseur*](gloss-p.md) , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="a411c-123">An instance of a CIM class that is supplied by a [*provider*](gloss-p.md) when required.</span></span> <span data-ttu-id="a411c-124">Elle n’est pas stockée dans le [*référentiel CIM*](gloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="a411c-124">It is not stored in the [*CIM repository*](gloss-c.md).</span></span> <span data-ttu-id="a411c-125">Les instances dynamiques peuvent être fournies pour des classes statiques ou dynamiques.</span><span class="sxs-lookup"><span data-stu-id="a411c-125">Dynamic instances can be provided for either static or dynamic classes.</span></span> <span data-ttu-id="a411c-126">La prise en charge dynamique des instances d’une classe permet à un fournisseur de fournir des valeurs de [*propriété*](gloss-p.md) à la minute.</span><span class="sxs-lookup"><span data-stu-id="a411c-126">Dynamically supporting instances of a class enables a provider to supply up-to-the-minute [*property*](gloss-p.md) values.</span></span>

</dd> </dl>

 

 



