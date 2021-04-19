---
description: Spécifie des informations sur un document associé à une opération DLP de point de terminaison.
title: Structure DLP_DOCUMENT_INFO (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_DOCUMENT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d588b627a4d5a88162cb0af67df1b5bf4fd943f1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495785"
---
# <a name="dlp_document_info-structure"></a><span data-ttu-id="dd457-103">Structure DLP_DOCUMENT_INFO</span><span class="sxs-lookup"><span data-stu-id="dd457-103">DLP_DOCUMENT_INFO structure</span></span>

<span data-ttu-id="dd457-104">Spécifie des informations sur un document associé à une opération DLP de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="dd457-104">Specifies information about a document that is associated with an endpoint DLP operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd457-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd457-105">Syntax</span></span>


```C++
typedef struct _DLP_DOCUMENT_INFO {

    DWORD Version;    
    LPCWSTR PersistentFileName;
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;
```


## <a name="members"></a><span data-ttu-id="dd457-106">Membres</span><span class="sxs-lookup"><span data-stu-id="dd457-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dd457-107">*Version* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="dd457-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd457-108">Valeur DWORD spécifiant la version de l’API.</span><span class="sxs-lookup"><span data-stu-id="dd457-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="dd457-109">Cette valeur doit toujours être **DLP_DOCUMENT_INFO_V_LATEST**.</span><span class="sxs-lookup"><span data-stu-id="dd457-109">This value should always be **DLP_DOCUMENT_INFO_V_LATEST**.</span></span> <span data-ttu-id="dd457-110">Cette constante est définie dans la liste des fichiers d’en-tête de l’exemple endpointdlp. h dans l’article [protection contre la perte de données](endpointdlp-endpoint-data-loss-prevention.md).</span><span class="sxs-lookup"><span data-stu-id="dd457-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md).</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="dd457-111">*PersistentFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd457-111">*PersistentFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd457-112">LPCWSTR spécifiant le chemin d’accès d’origine du document.</span><span class="sxs-lookup"><span data-stu-id="dd457-112">A LPCWSTR specifying the original path of the document.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="dd457-113">*LocalFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd457-113">*LocalFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd457-114">LPCWSTR spécifiant le chemin d’accès au fichier de sauvegarde réel du document.</span><span class="sxs-lookup"><span data-stu-id="dd457-114">A LPCWSTR specifying the path to the real backing file of the document.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="dd457-115">Notes</span><span class="sxs-lookup"><span data-stu-id="dd457-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="dd457-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dd457-116">Requirements</span></span>



| <span data-ttu-id="dd457-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd457-117">Requirement</span></span>          |    <span data-ttu-id="dd457-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd457-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd457-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd457-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dd457-120">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="dd457-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

