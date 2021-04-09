---
title: Fonctions de rappel ProjFS
description: Les fonctions de rappel suivantes sont déclarées dans projectedfslib. h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 1412fc4b406b668ad6651d69835f8cdea56857c5
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2020
ms.locfileid: "103841826"
---
# <a name="callback-functions"></a><span data-ttu-id="8fd19-103">Fonctions de rappel</span><span class="sxs-lookup"><span data-stu-id="8fd19-103">Callback functions</span></span>

<span data-ttu-id="8fd19-104">Les fonctions de rappel suivantes sont déclarées dans projectedfslib. h.</span><span class="sxs-lookup"><span data-stu-id="8fd19-104">The following callback functions are declared in projectedfslib.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8fd19-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="8fd19-105">In this section</span></span>

| <span data-ttu-id="8fd19-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="8fd19-106">Topic</span></span> | <span data-ttu-id="8fd19-107">Description</span><span class="sxs-lookup"><span data-stu-id="8fd19-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="8fd19-108">**PRJ_CANCEL_COMMAND_CB**</span><span class="sxs-lookup"><span data-stu-id="8fd19-108">**PRJ_CANCEL_COMMAND_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb) | <span data-ttu-id="8fd19-109">Notifie le fournisseur qu’une opération par un appel antérieur d’un rappel doit être annulée.</span><span class="sxs-lookup"><span data-stu-id="8fd19-109">Notifies the provider that an operation by an earlier invocation of a callback should be canceled.</span></span> |
| [<span data-ttu-id="8fd19-110">**PRJ_END_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="8fd19-110">**PRJ_END_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb) | <span data-ttu-id="8fd19-111">Informe le fournisseur qu’une énumération de répertoires est terminée.</span><span class="sxs-lookup"><span data-stu-id="8fd19-111">Informs the provider that a directory enumeration is over.</span></span> |
| [<span data-ttu-id="8fd19-112">**PRJ_GET_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="8fd19-112">**PRJ_GET_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb) | <span data-ttu-id="8fd19-113">Demande des informations sur l’énumération de répertoires à partir du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8fd19-113">Requests directory enumeration information from the provider.</span></span>
| [<span data-ttu-id="8fd19-114">**PRJ_GET_FILE_DATA_CB**</span><span class="sxs-lookup"><span data-stu-id="8fd19-114">**PRJ_GET_FILE_DATA_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb) | <span data-ttu-id="8fd19-115">Demande le contenu du flux de données principal d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="8fd19-115">Requests the contents of a file's primary data stream.</span></span>
| [<span data-ttu-id="8fd19-116">**PRJ_GET_PLACEHOLDER_INFO_CB**</span><span class="sxs-lookup"><span data-stu-id="8fd19-116">**PRJ_GET_PLACEHOLDER_INFO_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb) | <span data-ttu-id="8fd19-117">Demande des informations pour un fichier ou un répertoire du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8fd19-117">Requests information for a file or directory from the provider.</span></span>
| [<span data-ttu-id="8fd19-118">**PRJ_NOTIFICATION_CB**</span><span class="sxs-lookup"><span data-stu-id="8fd19-118">**PRJ_NOTIFICATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_notification_cb) | <span data-ttu-id="8fd19-119">Fournit des notifications au fournisseur sur les opérations du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="8fd19-119">Delivers notifications to the provider about file system operations.</span></span>
| [<span data-ttu-id="8fd19-120">**PRJ_QUERY_FILE_NAME_CB**</span><span class="sxs-lookup"><span data-stu-id="8fd19-120">**PRJ_QUERY_FILE_NAME_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_query_file_name_cb) | <span data-ttu-id="8fd19-121">Détermine si un chemin d’accès de fichier donné existe dans le magasin de stockage du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8fd19-121">Determines whether a given file path exists in the provider's backing store.</span></span>
| [<span data-ttu-id="8fd19-122">**PRJ_START_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="8fd19-122">**PRJ_START_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb) | <span data-ttu-id="8fd19-123">Informe le fournisseur qu’une énumération de répertoire est en cours de démarrage.</span><span class="sxs-lookup"><span data-stu-id="8fd19-123">Informs the provider that a directory enumeration is starting.</span></span>