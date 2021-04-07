---
title: Suppression d’une partition d’annuaire d’applications
description: Une partition d’annuaire d’applications est supprimée en supprimant l’objet crossRef qui représente la partition de l’annuaire d’applications.
ms.assetid: bc7986c1-5a11-440c-924e-dc525b5cb78f
ms.tgt_platform: multiple
keywords:
- Suppression d’une partition de l’annuaire d’applications Active Directory
- Partitions de l’annuaire d’applications Active Directory, suppression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd52ef99323ee7463a4733210314e02d911f0d66
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724573"
---
# <a name="deleting-an-application-directory-partition"></a><span data-ttu-id="93600-105">Suppression d’une partition d’annuaire d’applications</span><span class="sxs-lookup"><span data-stu-id="93600-105">Deleting an Application Directory Partition</span></span>

<span data-ttu-id="93600-106">Une partition d’annuaire d’applications est supprimée en supprimant l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) qui représente la partition de l’annuaire d’applications.</span><span class="sxs-lookup"><span data-stu-id="93600-106">An application directory partition is deleted by deleting the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that represents the application directory partition.</span></span> <span data-ttu-id="93600-107">Lorsque la suppression de l’objet **crossRef** est répliquée sur un contrôleur de domaine qui a un réplica de la partition de l’annuaire d’applications, le KCC supprime le réplica local de la partition de l’annuaire d’applications.</span><span class="sxs-lookup"><span data-stu-id="93600-107">When the deletion of the **crossRef** object replicates to a domain controller that has a replica of the application directory partition, the KCC will delete the local replica of the application directory partition.</span></span> <span data-ttu-id="93600-108">Cela finit par entraîner la suppression de tous les réplicas de la partition d’annuaire d’applications.</span><span class="sxs-lookup"><span data-stu-id="93600-108">This eventually causes all replicas of the application directory partition to be deleted.</span></span>

<span data-ttu-id="93600-109">Lorsque l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) est supprimé, le serveur de Active Directory supprime l’objet [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) qui a été créé lors de la création de la partition d’annuaire d’applications, ainsi que la suppression de tous les objets de la partition de l’annuaire d’applications.</span><span class="sxs-lookup"><span data-stu-id="93600-109">When the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object is deleted, the Active Directory server will delete the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object that was created when the application directory partition was created, as well as deleting all objects in the application directory partition.</span></span> <span data-ttu-id="93600-110">Aucun des objets de la partition de l’annuaire d’applications n’est désactivé lorsqu’ils sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="93600-110">None of the objects in the application directory partition are tombstoned when they deleted.</span></span>

<span data-ttu-id="93600-111">Lors de la suppression d’une partition d’annuaire d’applications, il est très difficile de la restaurer.</span><span class="sxs-lookup"><span data-stu-id="93600-111">When an application directory partition is deleted, it is very difficult to restore it.</span></span> <span data-ttu-id="93600-112">Pour restaurer une partition d’annuaire d’applications, il est nécessaire de restaurer une sauvegarde qui a un réplica de la partition d’annuaire d’applications, de Rechercher l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) qui représente la partition d’annuaire d’applications et de restaurer l’objet **crossRef** faisant autorité.</span><span class="sxs-lookup"><span data-stu-id="93600-112">To restore an application directory partition, it is necessary to restore a backup that has a replica of the application directory partition, find the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that represents the application directory partition and authoritatively restore the **crossRef** object.</span></span>

<span data-ttu-id="93600-113">**Pour supprimer une partition d’annuaire d’applications et ses réplicas, procédez comme suit :**</span><span class="sxs-lookup"><span data-stu-id="93600-113">**To delete an application directory partition and its replicas, perform the following steps**</span></span>

1.  <span data-ttu-id="93600-114">Recherchez dans le conteneur de partitions un objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) dont la valeur d’attribut [**NCName**](/windows/desktop/ADSchema/a-ncname) est égale au nom unique de la partition d’annuaire d’applications.</span><span class="sxs-lookup"><span data-stu-id="93600-114">Search the Partitions container for a [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that has an [**nCName**](/windows/desktop/ADSchema/a-ncname) attribute value that is equal to the distinguished name of the application directory partition.</span></span>
2.  <span data-ttu-id="93600-115">Supprimez l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) .</span><span class="sxs-lookup"><span data-stu-id="93600-115">Delete the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object.</span></span>

<span data-ttu-id="93600-116">Pour plus d’informations, consultez [exemple de code pour la suppression d’une partition d’annuaire d’applications](example-code-for-deleting-an-application-directory-partition.md).</span><span class="sxs-lookup"><span data-stu-id="93600-116">For more information, see [Example Code for Deleting an Application Directory Partition](example-code-for-deleting-an-application-directory-partition.md).</span></span>

 

 