---
description: Définition des droits d’administration pour une partition
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Définition des droits d’administration pour une partition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421b37dd50fa21ee9cf146749ec00b0c91d98c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748277"
---
# <a name="setting-administrative-rights-for-a-partition"></a><span data-ttu-id="fdd83-103">Définition des droits d’administration pour une partition</span><span class="sxs-lookup"><span data-stu-id="fdd83-103">Setting Administrative Rights for a Partition</span></span>

<span data-ttu-id="fdd83-104">Les utilisateurs disposant du rôle administrateur de l’application système COM+ sont autorisés à créer, modifier et supprimer des partitions COM+.</span><span class="sxs-lookup"><span data-stu-id="fdd83-104">Users assigned the Administrator role of the COM+ System Application are allowed to create, modify, and delete COM+ partitions.</span></span> <span data-ttu-id="fdd83-105">Dans l’outil d’administration Services de composants, les rôles administratifs peuvent être attribués aux utilisateurs en développant le dossier **rôles** de l’application système com+.</span><span class="sxs-lookup"><span data-stu-id="fdd83-105">Within the Component Services administrative tool, administrative roles can be assigned to users by expanding the **Roles** folder of the COM+ System Application.</span></span>

<span data-ttu-id="fdd83-106">À compter de Windows Server 2003, la fonctionnalité d’authentification de l’application système COM+ comprend la valeur EOAC \_ Disable \_ AAA.</span><span class="sxs-lookup"><span data-stu-id="fdd83-106">As of Windows Server 2003, the authentication capability for the COM+ System Application includes the value EOAC\_DISABLE\_AAA.</span></span> <span data-ttu-id="fdd83-107">Cette valeur, qui désactive les activations AAA (Activate-As-Activator), est utilisée dans l’appel de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) lors du lancement de l’application système.</span><span class="sxs-lookup"><span data-stu-id="fdd83-107">This value, which disables activate-as-activator (AAA) activations, is used in the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) call when launching the System Application.</span></span> <span data-ttu-id="fdd83-108">La définition de la fonctionnalité d’authentification sur EOAC \_ Disable \_ AAA permet à une application qui s’exécute sous un compte privilégié (tel que LocalSystem) d’empêcher son identité d’être utilisée pour lancer des composants non fiables.</span><span class="sxs-lookup"><span data-stu-id="fdd83-108">Setting the authentication capability to EOAC\_DISABLE\_AAA allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fdd83-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fdd83-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdd83-110">Collecte des métriques de partition</span><span class="sxs-lookup"><span data-stu-id="fdd83-110">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="fdd83-111">Configuration du cache de partition</span><span class="sxs-lookup"><span data-stu-id="fdd83-111">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="fdd83-112">Regroupement d’applications en partitions</span><span class="sxs-lookup"><span data-stu-id="fdd83-112">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="fdd83-113">Gestion des partitions locales</span><span class="sxs-lookup"><span data-stu-id="fdd83-113">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="fdd83-114">Gestion des partitions dans Active Directory</span><span class="sxs-lookup"><span data-stu-id="fdd83-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> </dl>

 

 
