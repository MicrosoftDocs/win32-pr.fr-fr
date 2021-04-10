---
description: Contient des informations utilisées lors de la création d’un contexte de tablette.
ms.assetid: 10466c23-f4cb-4205-886b-d85a2f530afe
title: Structure TABLET_CONTEXT_SETTINGS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_CONTEXT_SETTINGS
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9357281409ed4c48b4c6013a7a2be2997d58b094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953103"
---
# <a name="tablet_context_settings-structure"></a><span data-ttu-id="d8c80-103">Structure des paramètres de \_ contexte de tablette \_</span><span class="sxs-lookup"><span data-stu-id="d8c80-103">TABLET\_CONTEXT\_SETTINGS structure</span></span>

<span data-ttu-id="d8c80-104">Contient des informations utilisées lors de la création d’un contexte de tablette.</span><span class="sxs-lookup"><span data-stu-id="d8c80-104">Contains information used in creating a tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8c80-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8c80-105">Syntax</span></span>


```C++
typedef struct _TABLET_CONTEXT_SETTINGS {
  ULONG cPktProps;
  GUID  *pguidPktProps;
  ULONG cPktBtns;
  GUID  *pguidPktBtns;
  DWORD *pdwBtnDnMask;
  DWORD *pdwBtnUpMask;
  LONG  lXMargin;
  LONG  lYMargin;
} TABLET_CONTEXT_SETTINGS;
```



## <a name="members"></a><span data-ttu-id="d8c80-106">Membres</span><span class="sxs-lookup"><span data-stu-id="d8c80-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d8c80-107">**cPktProps**</span><span class="sxs-lookup"><span data-stu-id="d8c80-107">**cPktProps**</span></span>
</dt> <dd>

<span data-ttu-id="d8c80-108">Nombre de propriétés dans un paquet.</span><span class="sxs-lookup"><span data-stu-id="d8c80-108">The number of properties in a packet.</span></span>

</dd> <dt>

<span data-ttu-id="d8c80-109">**pguidPktProps**</span><span class="sxs-lookup"><span data-stu-id="d8c80-109">**pguidPktProps**</span></span>
</dt> <dd>

<span data-ttu-id="d8c80-110">Identificateurs uniques pour les propriétés du paquet.</span><span class="sxs-lookup"><span data-stu-id="d8c80-110">Unique identifiers for the packet properties.</span></span>

</dd> <dt>

<span data-ttu-id="d8c80-111">**cPktBtns**</span><span class="sxs-lookup"><span data-stu-id="d8c80-111">**cPktBtns**</span></span>
</dt> <dd>

<span data-ttu-id="d8c80-112">Nombre de boutons.</span><span class="sxs-lookup"><span data-stu-id="d8c80-112">The number of buttons.</span></span>

</dd> <dt>

<span data-ttu-id="d8c80-113">**pguidPktBtns**</span><span class="sxs-lookup"><span data-stu-id="d8c80-113">**pguidPktBtns**</span></span>
</dt> <dd>

<span data-ttu-id="d8c80-114">Identificateurs uniques pour les boutons.</span><span class="sxs-lookup"><span data-stu-id="d8c80-114">Unique identifiers for the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="d8c80-115">**pdwBtnDnMask**</span><span class="sxs-lookup"><span data-stu-id="d8c80-115">**pdwBtnDnMask**</span></span>
</dt> <dd>

<span data-ttu-id="d8c80-116">Masque de bouton enfoncé.</span><span class="sxs-lookup"><span data-stu-id="d8c80-116">The button down mask.</span></span>

</dd> <dt>

<span data-ttu-id="d8c80-117">**pdwBtnUpMask**</span><span class="sxs-lookup"><span data-stu-id="d8c80-117">**pdwBtnUpMask**</span></span>
</dt> <dd>

<span data-ttu-id="d8c80-118">Masque de bouton haut.</span><span class="sxs-lookup"><span data-stu-id="d8c80-118">The button up mask.</span></span>

</dd> <dt>

<span data-ttu-id="d8c80-119">**lXMargin**</span><span class="sxs-lookup"><span data-stu-id="d8c80-119">**lXMargin**</span></span>
</dt> <dd>

<span data-ttu-id="d8c80-120">Marge de direction X.</span><span class="sxs-lookup"><span data-stu-id="d8c80-120">The X direction margin.</span></span>

</dd> <dt>

<span data-ttu-id="d8c80-121">**lYMargin**</span><span class="sxs-lookup"><span data-stu-id="d8c80-121">**lYMargin**</span></span>
</dt> <dd>

<span data-ttu-id="d8c80-122">Marge de direction Y.</span><span class="sxs-lookup"><span data-stu-id="d8c80-122">The Y direction margin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8c80-123">Notes</span><span class="sxs-lookup"><span data-stu-id="d8c80-123">Remarks</span></span>

<span data-ttu-id="d8c80-124">En règle générale, une application obtient les valeurs par défaut à partir de la [**méthode ITablet :: GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifie les valeurs en fonction de leurs besoins, puis passe la structure des paramètres modifiés à la [**méthode ITablet :: CreateContext**](itablet-createcontext.md).</span><span class="sxs-lookup"><span data-stu-id="d8c80-124">Typically, an application obtains the default values from the [**ITablet::GetDefaultContextSettings Method**](itablet-getdefaultcontextsettings.md), modifies values to suit their needs, and then passes the modified settings structure to the [**ITablet::CreateContext Method**](itablet-createcontext.md).</span></span>

<span data-ttu-id="d8c80-125">Cette structure détermine les événements qu’une application obtiendra, la manière dont ils seront traités et la façon dont ils seront remis à l’application ou à Windows lui-même.</span><span class="sxs-lookup"><span data-stu-id="d8c80-125">This structure determines what events an application will get, how they will be processed, and how they will be delivered to the application or to Windows itself.</span></span>

<span data-ttu-id="d8c80-126">Les masques de bouton définissent ensemble les genres d’événements qui seront traités par le contexte.</span><span class="sxs-lookup"><span data-stu-id="d8c80-126">The button masks together determine what kinds of events will be processed by the context.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8c80-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8c80-127">Requirements</span></span>



| <span data-ttu-id="d8c80-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8c80-128">Requirement</span></span> | <span data-ttu-id="d8c80-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8c80-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d8c80-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8c80-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d8c80-131">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8c80-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d8c80-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8c80-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d8c80-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8c80-133">None supported</span></span><br/>                                     |



 

 




