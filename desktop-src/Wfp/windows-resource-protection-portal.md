---
description: La protection des ressources empêche le remplacement des fichiers système et des dossiers et des clés de Registre essentiels pour le système d’exploitation. La modification des ressources protégées peut entraîner une défaillance du système ou de l’application.
ms.assetid: 27df9300-8bea-4748-9acd-2c1625093ece
title: Protection des ressources Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff6c89e99b885256c7dd054a12c6a69795d794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319862"
---
# <a name="windows-resource-protection"></a><span data-ttu-id="d8c4a-104">Protection des ressources Windows</span><span class="sxs-lookup"><span data-stu-id="d8c4a-104">Windows Resource Protection</span></span>

## <a name="purpose"></a><span data-ttu-id="d8c4a-105">Objectif</span><span class="sxs-lookup"><span data-stu-id="d8c4a-105">Purpose</span></span>

<span data-ttu-id="d8c4a-106">Protection des ressources Windows (WRP) empêche le remplacement des fichiers système essentiels, des dossiers et des clés de Registre installés dans le cadre du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d8c4a-106">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of the operating system.</span></span> <span data-ttu-id="d8c4a-107">Il est devenu disponible à partir de Windows Server 2008 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d8c4a-107">It became available starting with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="d8c4a-108">Les applications ne doivent pas remplacer ces ressources, car elles sont utilisées par le système et d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="d8c4a-108">Applications should not overwrite these resources because they are used by the system and other applications.</span></span> <span data-ttu-id="d8c4a-109">La protection de ces ressources empêche les défaillances de l’application et du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d8c4a-109">Protecting these resources prevents application and operating system failures.</span></span> <span data-ttu-id="d8c4a-110">WRP est le nouveau nom de la protection de fichiers Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="d8c4a-110">WRP is the new name for Windows File Protection (WFP).</span></span> <span data-ttu-id="d8c4a-111">WRP protège les clés de Registre et les dossiers, ainsi que les fichiers système essentiels.</span><span class="sxs-lookup"><span data-stu-id="d8c4a-111">WRP protects registry keys and folders as well as essential system files.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="d8c4a-112">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="d8c4a-112">Where applicable</span></span>

<span data-ttu-id="d8c4a-113">Toutes les applications Windows et leurs programmes d’installation qui s’exécutent sur Windows Server 2008 ou Windows Vista, ainsi que sur les systèmes d’exploitation ultérieurs, doivent être conscients de WRP.</span><span class="sxs-lookup"><span data-stu-id="d8c4a-113">All Windows-based applications and their installation programs that run on Windows Server 2008 or Windows Vista, and later operating systems, should be aware of WRP.</span></span> <span data-ttu-id="d8c4a-114">Toutes les applications Windows qui s’exécutent sur Microsoft Windows Server 2003 ou Windows XP et leurs programmes d’installation doivent être conscientes de WFP.</span><span class="sxs-lookup"><span data-stu-id="d8c4a-114">All Windows-based applications that run on Microsoft Windows Server 2003 or Windows XP and their installation programs should be aware of WFP.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="d8c4a-115">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="d8c4a-115">Developer audience</span></span>

<span data-ttu-id="d8c4a-116">L’API WRP est conçue pour être utilisée par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="d8c4a-116">The WRP API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="d8c4a-117">L’API WRP a deux fonctions : [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) et [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).</span><span class="sxs-lookup"><span data-stu-id="d8c4a-117">The WRP API has two functions: [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) and [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d8c4a-118">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="d8c4a-118">Run-time requirements</span></span>

<span data-ttu-id="d8c4a-119">Les applications qui utilisent uniquement la fonction [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) nécessitent windows Server 2008, Windows Vista, windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d8c4a-119">Applications that use only the [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) function require Windows Server 2008, Windows Vista, Windows Server 2003, or Windows XP.</span></span> <span data-ttu-id="d8c4a-120">Les applications qui utilisent la fonction [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) nécessitent windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d8c4a-120">Applications that use the [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) function require Windows Server 2008 or Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d8c4a-121">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="d8c4a-121">In this section</span></span>



| <span data-ttu-id="d8c4a-122">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d8c4a-122">Topic</span></span>                                                                                     | <span data-ttu-id="d8c4a-123">Description</span><span class="sxs-lookup"><span data-stu-id="d8c4a-123">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="d8c4a-124">À propos de Protection des ressources Windows</span><span class="sxs-lookup"><span data-stu-id="d8c4a-124">About Windows Resource Protection</span></span>](about-windows-file-protection.md)<br/>         | <span data-ttu-id="d8c4a-125">Informations générales sur WRP.</span><span class="sxs-lookup"><span data-stu-id="d8c4a-125">General information about WRP.</span></span><br/>   |
| [<span data-ttu-id="d8c4a-126">Référence Protection des ressources Windows</span><span class="sxs-lookup"><span data-stu-id="d8c4a-126">Windows Resource Protection Reference</span></span>](windows-file-protection-reference.md)<br/> | <span data-ttu-id="d8c4a-127">Documentation de référence pour WRP.</span><span class="sxs-lookup"><span data-stu-id="d8c4a-127">Reference documentation for WRP.</span></span><br/> |



 

 

 




