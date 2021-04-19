---
description: Répertorie les types de données utilisés par les dll d’attachement de configuration de sécurité et leurs fonctions de prise en charge.
ms.assetid: 1d3bdf0d-320c-4b25-9e9b-fda134876979
title: Types de données de gestion de la sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7efedb32ab545b903c61819042e32b7d83dbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524253"
---
# <a name="security-management-data-types"></a><span data-ttu-id="71ffe-103">Types de données de gestion de la sécurité</span><span class="sxs-lookup"><span data-stu-id="71ffe-103">Security Management Data Types</span></span>

<span data-ttu-id="71ffe-104">Les types de données de gestion de la sécurité sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="71ffe-104">The security management data types include the following:</span></span>

-   [<span data-ttu-id="71ffe-105">Types de données de pièce jointe</span><span class="sxs-lookup"><span data-stu-id="71ffe-105">Attachment Data Types</span></span>](#attachment-data-types)
-   [<span data-ttu-id="71ffe-106">Types de données de la stratégie LSA</span><span class="sxs-lookup"><span data-stu-id="71ffe-106">LSA Policy Data Types</span></span>](#lsa-policy-data-types)

## <a name="attachment-data-types"></a><span data-ttu-id="71ffe-107">Types de données de pièce jointe</span><span class="sxs-lookup"><span data-stu-id="71ffe-107">Attachment Data Types</span></span>

<span data-ttu-id="71ffe-108">Les types de données suivants sont utilisés par les dll de la configuration de sécurité jointes et leurs fonctions de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="71ffe-108">The following data types are used by the Security Configuration attachment DLLs and their supporting functions.</span></span>



| <span data-ttu-id="71ffe-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="71ffe-109">Data type</span></span>                                                    | <span data-ttu-id="71ffe-110">Description</span><span class="sxs-lookup"><span data-stu-id="71ffe-110">Description</span></span>                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71ffe-111">**\_contexte d’énumération SCE \_**</span><span class="sxs-lookup"><span data-stu-id="71ffe-111">**SCE\_ENUMERATION\_CONTEXT**</span></span>](sce-enumeration-context.md) | <span data-ttu-id="71ffe-112">Utilisé par la fonction [**PFSCE \_ query \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) pour naviguer dans la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="71ffe-112">Used by the [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) function to navigate through the security database.</span></span>                                                                                                                                              |
| [<span data-ttu-id="71ffe-113">**\_handle SCE**</span><span class="sxs-lookup"><span data-stu-id="71ffe-113">**SCE\_HANDLE**</span></span>](sce-handle.md)                            | <span data-ttu-id="71ffe-114">Utilisé par [**PFSCE \_ query \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) et [**PFSCE \_ Set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) pour transmettre des informations entre la pièce jointe et la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="71ffe-114">Used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) to pass information between the attachment and the security database.</span></span>                                                                                 |
| [<span data-ttu-id="71ffe-115">**SCESTATUS**</span><span class="sxs-lookup"><span data-stu-id="71ffe-115">**SCESTATUS**</span></span>](scestatus.md)                               | <span data-ttu-id="71ffe-116">Le type de données est utilisé par l’API Set de l’outil de configuration de la sécurité pour retourner des informations sur les résultats d’un appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="71ffe-116">Data type is used by the Security Configuration tool set API to return information about the results of a function call.</span></span>                                                                                                                                    |
| [<span data-ttu-id="71ffe-117">**\_handle SCESVC**</span><span class="sxs-lookup"><span data-stu-id="71ffe-117">**SCESVC\_HANDLE**</span></span>](scesvc-handle.md)                      | <span data-ttu-id="71ffe-118">Utilisé par les méthodes des interfaces [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) et [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) pour passer des informations entre le composant logiciel enfichable Configuration de la sécurité et l’extension du composant logiciel enfichable.</span><span class="sxs-lookup"><span data-stu-id="71ffe-118">Used by methods of the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) and [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interfaces to pass information between the Security Configuration snap-in and the snap-in extension.</span></span> |
| [<span data-ttu-id="71ffe-119">**\_type d’informations SCESVC \_**</span><span class="sxs-lookup"><span data-stu-id="71ffe-119">**SCESVC\_INFO\_TYPE**</span></span>](/windows/desktop/api/Scesvc/ne-scesvc-scesvc_info_type)               | <span data-ttu-id="71ffe-120">L’énumération est utilisée par les informations de [**\_ requête \_ PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) et [**PFSCE \_ Set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) pour indiquer le type d’informations demandées ou transmises à la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="71ffe-120">Enumeration is used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) to indicate the type of information requested from or passed to the security database.</span></span>                                                 |



 

## <a name="lsa-policy-data-types"></a><span data-ttu-id="71ffe-121">Types de données de la stratégie LSA</span><span class="sxs-lookup"><span data-stu-id="71ffe-121">LSA Policy Data Types</span></span>

<span data-ttu-id="71ffe-122">Les types de données suivants sont utilisés par les fonctions de gestion de la stratégie LSA.</span><span class="sxs-lookup"><span data-stu-id="71ffe-122">The following data types are used by the LSA policy management functions.</span></span>



| <span data-ttu-id="71ffe-123">Type de données</span><span class="sxs-lookup"><span data-stu-id="71ffe-123">Data type</span></span>                                                  | <span data-ttu-id="71ffe-124">Description</span><span class="sxs-lookup"><span data-stu-id="71ffe-124">Description</span></span>                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="71ffe-125">**\_handle d’énumération LSA \_**</span><span class="sxs-lookup"><span data-stu-id="71ffe-125">**LSA\_ENUMERATION\_HANDLE**</span></span>](lsa-enumeration-handle.md) | <span data-ttu-id="71ffe-126">Utilisé pour suivre les énumérations dans lesquelles plusieurs appels de fonction sont requis.</span><span class="sxs-lookup"><span data-stu-id="71ffe-126">Used to track enumerations in which multiple function calls are required.</span></span> |
| [<span data-ttu-id="71ffe-127">**\_handle LSA**</span><span class="sxs-lookup"><span data-stu-id="71ffe-127">**LSA\_HANDLE**</span></span>](lsa-handle.md)                          | <span data-ttu-id="71ffe-128">Handle vers un objet de [**stratégie**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="71ffe-128">Handle to a [**Policy**](policy-object.md) object.</span></span>                       |



 

 

 
