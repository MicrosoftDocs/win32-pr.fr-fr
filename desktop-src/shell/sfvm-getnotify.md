---
description: Notification envoyée à l’objet de rappel d’affichage pour spécifier les emplacements et les événements qui doivent être enregistrés pour les événements de notification de modification.
title: Message SFVM_GETNOTIFY (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87933217-dfa9-4aaf-9630-fa2c302b18fa
api_name:
- SFVM_GETNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f766ee74463dd820c0b55d501d5002a3378a97b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203670"
---
# <a name="sfvm_getnotify-message"></a><span data-ttu-id="b18e7-103">\_Message SFVM GETNOTIFY</span><span class="sxs-lookup"><span data-stu-id="b18e7-103">SFVM\_GETNOTIFY message</span></span>

<span data-ttu-id="b18e7-104">Notification envoyée à l’objet de rappel d’affichage pour spécifier les emplacements et les événements qui doivent être enregistrés pour les événements de notification de modification.</span><span class="sxs-lookup"><span data-stu-id="b18e7-104">Notification sent to the view callback object to specify the locations and events that should be registered for change notification events.</span></span> <span data-ttu-id="b18e7-105">Une fois qu’ils sont inscrits, quand une modification se produit dans sur ces emplacements ou événements, l’objet de rappel de vue est notifié.</span><span class="sxs-lookup"><span data-stu-id="b18e7-105">Once they are registered, when a change occurs in on of these locations or events, the view callback object is notified.</span></span> <span data-ttu-id="b18e7-106">Ces événements sont envoyés au rappel de la vue via [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) et sont ensuite gérés par la vue.</span><span class="sxs-lookup"><span data-stu-id="b18e7-106">These events are sent to the view callback through [**SFVM\_FSNOTIFY**](sfvm-fsnotify.md) and are then handled by the view.</span></span>


```C++
SFVM_GETNOTIFY 

    wParam = (WPARAM)(LPITEMIDLIST*) pidl;

    lParam = (LPARAM)(LONG*) lEvents;

            
```



## <a name="parameters"></a><span data-ttu-id="b18e7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b18e7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b18e7-108">*PIDL* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b18e7-108">*pidl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b18e7-109">Pointeur vers un IDList absolu d’un élément pour lequel la vue doit s’inscrire pour être avertie des modifications.</span><span class="sxs-lookup"><span data-stu-id="b18e7-109">A pointer to an absolute IDList of an item for which the view should register to be notified of changes.</span></span> <span data-ttu-id="b18e7-110">En règle générale, il s’agit du même IDList que l’emplacement affiché, mais il peut s’agir d’un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="b18e7-110">Typically, this is the same as the IDList of the location being viewed, but it can be another location.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b18e7-111">La durée de vie de cette valeur est la propriété de l’objet de rappel de la vue.</span><span class="sxs-lookup"><span data-stu-id="b18e7-111">The lifetime of this value is owned by the view callback object.</span></span> <span data-ttu-id="b18e7-112">Il est de la responsabilité de l’objet de rappel de vue de créer, puis de libérer cette valeur lorsqu’il n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b18e7-112">It is the responsibility of the view callback object to create and then free this value when it is no longer needed.</span></span> <span data-ttu-id="b18e7-113">Cela nécessite que l’objet de rappel de vue stocke cette valeur.</span><span class="sxs-lookup"><span data-stu-id="b18e7-113">This requires that the view callback object stores this value.</span></span> <span data-ttu-id="b18e7-114">En règle générale, la valeur peut être stockée dans le membre **\_ pidlMonitor** de l’objet de rappel de la vue.</span><span class="sxs-lookup"><span data-stu-id="b18e7-114">Usually, the value can be stored in the **\_pidlMonitor** member of the view callback object.</span></span> <span data-ttu-id="b18e7-115">Les règles de propriété pour la valeur retournée via *PIDL* sont non standard et nécessitent une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="b18e7-115">The ownership rules for the value returned through *pidl* are nonstandard and require special care.</span></span> <span data-ttu-id="b18e7-116">L’objet de rappel de vue doit posséder cette valeur et s’assurer qu’il n’est pas libéré tant que l’objet de rappel d’affichage lui-même n’est pas détruit.</span><span class="sxs-lookup"><span data-stu-id="b18e7-116">The view callback object must own this value and ensure that it is not freed until the view callback object itself is destroyed.</span></span>

 

</dd> <dt>

<span data-ttu-id="b18e7-117">*lEvents* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b18e7-117">*lEvents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b18e7-118">Valeur qui contient une ou plusieurs valeurs SHCNE.</span><span class="sxs-lookup"><span data-stu-id="b18e7-118">A value that contains one or more SHCNE values.</span></span> <span data-ttu-id="b18e7-119">Pour obtenir la liste des valeurs possibles, consultez [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) .</span><span class="sxs-lookup"><span data-stu-id="b18e7-119">See [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) for a list of possible values.</span></span> <span data-ttu-id="b18e7-120">L’objet de rappel d’affichage s’inscrit pour recevoir un message [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) lorsque l’un des événements associés se produit.</span><span class="sxs-lookup"><span data-stu-id="b18e7-120">The view callback object will register to receive an [**SFVM\_FSNOTIFY**](sfvm-fsnotify.md) message when any of the associated events occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b18e7-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b18e7-121">Return value</span></span>

<span data-ttu-id="b18e7-122">Ignoré, mais doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b18e7-122">Ignored, but should return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b18e7-123">Notes</span><span class="sxs-lookup"><span data-stu-id="b18e7-123">Remarks</span></span>

<span data-ttu-id="b18e7-124">Si ce message de rappel ne retourne pas une valeur différente de zéro pour le IDList ou le masque d’événements, la vue n’est pas inscrite pour les notifications de modification.</span><span class="sxs-lookup"><span data-stu-id="b18e7-124">If this callback message does not return a nonzero value for either the IDList or the events mask then the view will not register for change notifications.</span></span>

## <a name="examples"></a><span data-ttu-id="b18e7-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="b18e7-125">Examples</span></span>

<span data-ttu-id="b18e7-126">L’exemple suivant montre un exemple d’implémentation du code du gestionnaire de la fonction de rappel d’affichage pour **SFVM \_ GETNOTIFY**.</span><span class="sxs-lookup"><span data-stu-id="b18e7-126">The following sample shows an example implementation of the view callback function's handler code for **SFVM\_GETNOTIFY**.</span></span>


```C++
case SFVM_GETNOTIFY:
  *((LPITEMIDLIST*)wParam) = _pidl;    // Pass a reference whose lifetime this 
                                       // class is responsible for.
                                      
  *((LONG*)lParam) = SHCNE_DISKEVENTS; // A combination of all of the 
                                       // disk event identifiers.
                                       
   return S_OK;
```



## <a name="requirements"></a><span data-ttu-id="b18e7-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b18e7-127">Requirements</span></span>



| <span data-ttu-id="b18e7-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b18e7-128">Requirement</span></span> | <span data-ttu-id="b18e7-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b18e7-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b18e7-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b18e7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b18e7-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b18e7-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b18e7-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b18e7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b18e7-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b18e7-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b18e7-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="b18e7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b18e7-135"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="b18e7-135"><dt>Shlobj.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b18e7-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b18e7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b18e7-137">**SFVM \_ QUERYFSNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="b18e7-137">**SFVM\_QUERYFSNOTIFY**</span></span>](sfvm-queryfsnotify.md)
</dt> <dt>

[<span data-ttu-id="b18e7-138">**IShellFolderViewCB::MessageSFVCB**</span><span class="sxs-lookup"><span data-stu-id="b18e7-138">**IShellFolderViewCB::MessageSFVCB**</span></span>](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)
</dt> </dl>

 

 
