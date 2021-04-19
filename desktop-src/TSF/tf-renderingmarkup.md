---
title: Structure TF_RENDERINGMARKUP
description: La structure de la \_ structure RENDERINGMARKUP TF contient une plage et les informations d’attribut d’affichage.
ms.assetid: 206e679b-f2eb-4f28-ac2a-58f3c222a020
keywords:
- TF_RENDERINGMARKUP structure Text Services Framework
topic_type:
- apiref
api_name:
- TF_RENDERINGMARKUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 166a60182ae7b53dbc70993a7bae81991e42255b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106512071"
---
# <a name="tf_renderingmarkup-structure"></a><span data-ttu-id="9756e-104">\_Structure RENDERINGMARKUP TF</span><span class="sxs-lookup"><span data-stu-id="9756e-104">TF\_RENDERINGMARKUP structure</span></span>

<span data-ttu-id="9756e-105">La structure de la structure [**\_ RENDERINGMARKUP TF**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) contient une plage et les informations d’attribut d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9756e-105">The [**TF\_RENDERINGMARKUP**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) structure structure contains a range and the display attribute information.</span></span>

## <a name="syntax"></a><span data-ttu-id="9756e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9756e-106">Syntax</span></span>


```C++
typedef struct {
  ITfRange*           pRange;
  TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;
```



## <a name="members"></a><span data-ttu-id="9756e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="9756e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9756e-108">**pRange**</span><span class="sxs-lookup"><span data-stu-id="9756e-108">**pRange**</span></span>
</dt> <dd>

<span data-ttu-id="9756e-109">Pointeur vers une interface [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) .</span><span class="sxs-lookup"><span data-stu-id="9756e-109">A pointer to an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) interface.</span></span>

</dd> <dt>

<span data-ttu-id="9756e-110">**tfDisplayAttr**</span><span class="sxs-lookup"><span data-stu-id="9756e-110">**tfDisplayAttr**</span></span>
</dt> <dd>

<span data-ttu-id="9756e-111">Affichez les informations d’attribut.</span><span class="sxs-lookup"><span data-stu-id="9756e-111">Display attribute information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9756e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="9756e-112">Remarks</span></span>

<span data-ttu-id="9756e-113">Cette structure n’est pas actuellement dans les fichiers d’en-tête publics.</span><span class="sxs-lookup"><span data-stu-id="9756e-113">This structure is not currently in the public header files.</span></span> <span data-ttu-id="9756e-114">Pour utiliser cette API, vous devez effectuer une compilation MIDL du [prototype](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="9756e-114">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 




