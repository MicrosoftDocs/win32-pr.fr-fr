---
description: Spécifie des informations sur un document associé à une opération d’impression DLP de point de terminaison.
title: Structure DLP_PRINT_INFO (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_PRINT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 37bde9f62de07083aac6a3d2fb367b021caf3732
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495778"
---
# <a name="dlp_print_info-structure"></a><span data-ttu-id="24f73-103">Structure DLP_PRINT_INFO</span><span class="sxs-lookup"><span data-stu-id="24f73-103">DLP_PRINT_INFO structure</span></span>

<span data-ttu-id="24f73-104">Spécifie des informations sur un document associé à une opération d’impression DLP de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="24f73-104">Specifies information about a document that is associated with an endpoint DLP print operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="24f73-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24f73-105">Syntax</span></span>


```C++
typedef struct _DLP_PRINT_INFO {
    DWORD Version;
    LPCWSTR PrinterName;
    LPCWSTR JobName;
    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;
```


## <a name="members"></a><span data-ttu-id="24f73-106">Membres</span><span class="sxs-lookup"><span data-stu-id="24f73-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="24f73-107">*Version* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="24f73-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f73-108">Valeur DWORD spécifiant la version de l’API.</span><span class="sxs-lookup"><span data-stu-id="24f73-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="24f73-109">Cette valeur doit toujours être **DLP_PRINT_INFO_V_LATEST**.</span><span class="sxs-lookup"><span data-stu-id="24f73-109">This value should always be **DLP_PRINT_INFO_V_LATEST**.</span></span> <span data-ttu-id="24f73-110">Cette constante est définie dans la liste des fichiers d’en-tête de l’exemple endpointdlp. h dans l’article [protection contre la perte de données](endpointdlp-endpoint-data-loss-prevention.md).</span><span class="sxs-lookup"><span data-stu-id="24f73-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md).</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="24f73-111">*Nom_imprimante* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="24f73-111">*PrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f73-112">LPCWSTR identifiant l’imprimante de destination.</span><span class="sxs-lookup"><span data-stu-id="24f73-112">A LPCWSTR identifying the destination printer.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="24f73-113">*JobName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="24f73-113">*JobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f73-114">LPCWSTR spécifiant le nom du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="24f73-114">A LPCWSTR specifying print job name.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="24f73-115">*OutputFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="24f73-115">*OutputFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f73-116">LPCWSTR spécifiant le chemin d’accès au fichier de sortie, lors de l’impression dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="24f73-116">A LPCWSTR specifying the path to the output file, when printing to a file.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="24f73-117">Notes</span><span class="sxs-lookup"><span data-stu-id="24f73-117">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="24f73-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="24f73-118">Requirements</span></span>



| <span data-ttu-id="24f73-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24f73-119">Requirement</span></span>          |    <span data-ttu-id="24f73-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="24f73-120">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24f73-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24f73-121">Minimum supported client</span></span><br/> | <span data-ttu-id="24f73-122">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="24f73-122">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

