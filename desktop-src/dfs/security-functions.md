---
title: Fonctions de sécurité
description: Les fonctions de sécurité de la gestion du réseau obtiennent et définissent des descripteurs de sécurité pour les racines de domaine et autonomes DFS.
ms.assetid: 90860842-0f4d-49ad-b835-50305328a050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f717ff3f5701e507087fcdac164d9357f2505a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483848"
---
# <a name="security-functions"></a><span data-ttu-id="b54a8-103">Fonctions de sécurité</span><span class="sxs-lookup"><span data-stu-id="b54a8-103">Security Functions</span></span>

<span data-ttu-id="b54a8-104">Les fonctions de sécurité de la gestion du réseau obtiennent et définissent des descripteurs de sécurité pour les racines de domaine et autonomes DFS.</span><span class="sxs-lookup"><span data-stu-id="b54a8-104">The network management security functions get and set security descriptors for DFS domain-based and stand-alone roots.</span></span>

<span data-ttu-id="b54a8-105">Les fonctions de sécurité DFS sont répertoriées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b54a8-105">The DFS security functions are listed following.</span></span>

| <span data-ttu-id="b54a8-106">Fonction</span><span class="sxs-lookup"><span data-stu-id="b54a8-106">Function</span></span>                                                               | <span data-ttu-id="b54a8-107">Description</span><span class="sxs-lookup"><span data-stu-id="b54a8-107">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b54a8-108">**NetDfsGetSecurity**</span><span class="sxs-lookup"><span data-stu-id="b54a8-108">**NetDfsGetSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)                         | <span data-ttu-id="b54a8-109">Obtient le descripteur de sécurité pour l’objet racine de la racine DFS spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b54a8-109">Obtains the security descriptor for the root object of the specified DFS root.</span></span>                                       |
| [<span data-ttu-id="b54a8-110">**NetDfsSetSecurity**</span><span class="sxs-lookup"><span data-stu-id="b54a8-110">**NetDfsSetSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)                         | <span data-ttu-id="b54a8-111">Localise l’objet racine pour la racine DFS spécifiée et définit le descripteur de sécurité fourni dessus.</span><span class="sxs-lookup"><span data-stu-id="b54a8-111">Locates the root object for the specified DFS root and sets the supplied security descriptor on it.</span></span>                  |
| [<span data-ttu-id="b54a8-112">**NetDfsGetStdContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="b54a8-112">**NetDfsGetStdContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity) | <span data-ttu-id="b54a8-113">Obtient le descripteur de sécurité pour l’objet conteneur de la racine autonome DFS spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b54a8-113">Obtains the security descriptor for the container object of the specified DFS stand-alone root.</span></span>                      |
| [<span data-ttu-id="b54a8-114">**NetDfsSetStdContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="b54a8-114">**NetDfsSetStdContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity) | <span data-ttu-id="b54a8-115">Localise l’objet conteneur pour la racine autonome DFS spécifiée et définit le descripteur de sécurité fourni dessus.</span><span class="sxs-lookup"><span data-stu-id="b54a8-115">Locates the container object for the specified DFS stand-alone root and sets the supplied security descriptor on it.</span></span> |
| [<span data-ttu-id="b54a8-116">**NetDfsGetFtContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="b54a8-116">**NetDfsGetFtContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)   | <span data-ttu-id="b54a8-117">Obtient le descripteur de sécurité pour l’objet conteneur de la racine du domaine DFS spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b54a8-117">Obtains the security descriptor for the container object of the specified DFS domain root.</span></span>                           |
| [<span data-ttu-id="b54a8-118">**NetDfsSetFtContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="b54a8-118">**NetDfsSetFtContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)   | <span data-ttu-id="b54a8-119">Localise l’objet conteneur pour la racine de domaine DFS spécifiée et définit le descripteur de sécurité fourni dessus.</span><span class="sxs-lookup"><span data-stu-id="b54a8-119">Locates the container object for the specified DFS domain root and sets the supplied security descriptor on it.</span></span>      |
