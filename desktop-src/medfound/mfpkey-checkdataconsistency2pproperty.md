---
description: Spécifie si l’encodeur doit vérifier la cohérence des données entre les passes lors de l’exécution du codage VBR en deux passes. Lecture-écriture.
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: MFPKEY_CHECKDATACONSISTENCY2P, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc706712ef1e8bff36a118031fde155bb9bda31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525349"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a><span data-ttu-id="fbd3f-104">MFPKEY \_ propriété CHECKDATACONSISTENCY2P</span><span class="sxs-lookup"><span data-stu-id="fbd3f-104">MFPKEY\_CHECKDATACONSISTENCY2P Property</span></span>

<span data-ttu-id="fbd3f-105">Spécifie si l’encodeur doit vérifier la cohérence des données entre les passes lors de l’exécution du codage VBR en deux passes.</span><span class="sxs-lookup"><span data-stu-id="fbd3f-105">Specifies whether whether the encoder should check for data consistency across passes when performing two-pass VBR encoding.</span></span> <span data-ttu-id="fbd3f-106">Lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="fbd3f-106">Read-write.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="fbd3f-107">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="fbd3f-107">Constant for IPropertyBag</span></span>

<span data-ttu-id="fbd3f-108">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="fbd3f-108">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="fbd3f-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="fbd3f-109">Data Type</span></span>

<span data-ttu-id="fbd3f-110">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="fbd3f-110">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="fbd3f-111">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fbd3f-111">Default Value</span></span>

<span data-ttu-id="fbd3f-112">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="fbd3f-112">**VARIANT\_TRUE**</span></span>

## <a name="remarks"></a><span data-ttu-id="fbd3f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="fbd3f-113">Remarks</span></span>

<span data-ttu-id="fbd3f-114">Si vous laissez cette propriété à sa valeur par défaut **Variant \_ true**, l’encodeur vérifie que les exemples d’entrée correspondent entre les deux passes et échoue s’il détecte une incohérence.</span><span class="sxs-lookup"><span data-stu-id="fbd3f-114">If you leave this property at its default value of **VARIANT\_TRUE**, the encoder verifies that the input samples match between the two passes, and fails if it detects a discrepancy.</span></span> <span data-ttu-id="fbd3f-115">Le scénario principal qui provoque une incohérence est lorsque l’entrée provient d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="fbd3f-115">The main scenario that leads to a discrepancy is when the input comes from a device.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbd3f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbd3f-116">Requirements</span></span>



| <span data-ttu-id="fbd3f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbd3f-117">Requirement</span></span> | <span data-ttu-id="fbd3f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbd3f-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbd3f-119">Client</span><span class="sxs-lookup"><span data-stu-id="fbd3f-119">Client</span></span><br/> | <span data-ttu-id="fbd3f-120">Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="fbd3f-120">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="fbd3f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="fbd3f-121">Header</span></span><br/> | <dl> <span data-ttu-id="fbd3f-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbd3f-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbd3f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbd3f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbd3f-124">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fbd3f-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
