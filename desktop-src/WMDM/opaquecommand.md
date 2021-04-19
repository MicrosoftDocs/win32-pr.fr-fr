---
title: OPAQUECOMMAND, structure
description: La structure OPAQUECOMMAND contient des données pour les commandes qui sont transmises par le biais de Windows Media Gestionnaire de périphériques à un appareil, mais qui ne sont pas destinées à être traitées par Windows Media Gestionnaire de périphériques.
ms.assetid: 5b39cf07-2816-4615-a754-e3f0c57bf4ce
keywords:
- Structure OPAQUECOMMAND Windows Media Gestionnaire de périphériques
- structure du Gestionnaire de périphériques Windows Media
topic_type:
- apiref
api_name:
- OPAQUECOMMAND
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672147cb99336f95a1ced88a3cc6b8df977aec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545484"
---
# <a name="opaquecommand-structure"></a><span data-ttu-id="4330e-105">OPAQUECOMMAND, structure</span><span class="sxs-lookup"><span data-stu-id="4330e-105">OPAQUECOMMAND structure</span></span>

<span data-ttu-id="4330e-106">La structure **OPAQUECOMMAND** contient des données pour les commandes qui sont transmises par le biais de windows media gestionnaire de périphériques à un appareil, mais qui ne sont pas destinées à être traitées par windows media gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="4330e-106">The **OPAQUECOMMAND** structure contains data for commands that are passed through Windows Media Device Manager to a device but are not intended to be acted upon by Windows Media Device Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="4330e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4330e-107">Syntax</span></span>


```C++
typedef struct OPAQUECOMMAND {
  GUID  guidCommand;
  DWORD dwDataLen;
  BYTE  *pData;
  BYTE  abMAC[20];
} ;
```



## <a name="members"></a><span data-ttu-id="4330e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4330e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4330e-109">**guidCommand**</span><span class="sxs-lookup"><span data-stu-id="4330e-109">**guidCommand**</span></span>
</dt> <dd>

<span data-ttu-id="4330e-110">**GUID** représentant la commande demandée.</span><span class="sxs-lookup"><span data-stu-id="4330e-110">**GUID** representing the requested command.</span></span>

</dd> <dt>

<span data-ttu-id="4330e-111">**dwDataLen**</span><span class="sxs-lookup"><span data-stu-id="4330e-111">**dwDataLen**</span></span>
</dt> <dd>

<span data-ttu-id="4330e-112">Longueur des données vers laquelle *pData* pointe, en octets.</span><span class="sxs-lookup"><span data-stu-id="4330e-112">Length of the data to which *pData* points, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4330e-113">**pData**</span><span class="sxs-lookup"><span data-stu-id="4330e-113">**pData**</span></span>
</dt> <dd>

<span data-ttu-id="4330e-114">Données requises pour exécuter la commande et/ou les données retournées par la commande.</span><span class="sxs-lookup"><span data-stu-id="4330e-114">Data required to execute the command, and/or data returned by the command.</span></span>

</dd> <dt>

<span data-ttu-id="4330e-115">**abMAC \[ 20\]**</span><span class="sxs-lookup"><span data-stu-id="4330e-115">**abMAC\[20\]**</span></span>
</dt> <dd>

<span data-ttu-id="4330e-116">Ce code d’authentification de message (MAC) doit inclure le membre **guidCommand** , les données auxquelles *pdwDataLen* pointe, ainsi que les données auxquelles *pData* pointe, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="4330e-116">This message authentication code (MAC) should include the **guidCommand** member, the data to which *pdwDataLen* points, and the data to which *pData* points, if any.</span></span> <span data-ttu-id="4330e-117">Si *pData* a la **valeur null**, il ne doit pas être inclus dans le Mac.</span><span class="sxs-lookup"><span data-stu-id="4330e-117">If *pData* is **NULL**, it must not be included in the MAC.</span></span> <span data-ttu-id="4330e-118">La \_ longueur WMDM Mac \_ est définie sur 20.</span><span class="sxs-lookup"><span data-stu-id="4330e-118">WMDM\_MAC\_LENGTH is defined as 20.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4330e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4330e-119">Requirements</span></span>



| <span data-ttu-id="4330e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4330e-120">Requirement</span></span> | <span data-ttu-id="4330e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4330e-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4330e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="4330e-122">Header</span></span><br/> | <dl> <span data-ttu-id="4330e-123"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4330e-123"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4330e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4330e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4330e-125">**IMDSPDevice::SendOpaqueCommand**</span><span class="sxs-lookup"><span data-stu-id="4330e-125">**IMDSPDevice::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="4330e-126">**IMDSPStorage::SendOpaqueCommands**</span><span class="sxs-lookup"><span data-stu-id="4330e-126">**IMDSPStorage::SendOpaqueCommands**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="4330e-127">**IWMDMDevice::SendOpaqueCommand**</span><span class="sxs-lookup"><span data-stu-id="4330e-127">**IWMDMDevice::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="4330e-128">**IWMDMStorage::SendOpaqueCommand**</span><span class="sxs-lookup"><span data-stu-id="4330e-128">**IWMDMStorage::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="4330e-129">**Structures**</span><span class="sxs-lookup"><span data-stu-id="4330e-129">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





