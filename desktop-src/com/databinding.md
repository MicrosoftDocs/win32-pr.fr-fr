---
title: Liaison de données
description: Liaison de données
ms.assetid: 7fc5f036-8b36-4e0e-a257-173010fe127a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec6b8e66300834939a2b65fddefe947781350b0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106509879"
---
# <a name="databinding"></a><span data-ttu-id="1d7d2-103">Liaison de données</span><span class="sxs-lookup"><span data-stu-id="1d7d2-103">Databinding</span></span>

<span data-ttu-id="1d7d2-104">Un nouvel attribut DataBinding a été ajouté pour permettre aux propriétés de faire la distinction entre les modifications de communication uniquement lorsque le focus quitte le contrôle ou pendant toutes les notifications de modification de propriété.</span><span class="sxs-lookup"><span data-stu-id="1d7d2-104">A new databinding attribute has been added to allow properties distinguish between communicating changes only when focus leaves the control or during all property change notifications.</span></span>

<span data-ttu-id="1d7d2-105">Le nouvel attribut, connu sous le nom de ImmediateBind, permet aux contrôles de différencier deux types différents de propriétés pouvant être liées.</span><span class="sxs-lookup"><span data-stu-id="1d7d2-105">The new attribute, known as ImmediateBind, enables controls to differentiate two different types of bindable properties.</span></span> <span data-ttu-id="1d7d2-106">Un type de propriété pouvant être liée doit notifier chaque modification apportée à la base de données, par exemple avec un contrôle de case à cocher où chaque modification doit être envoyée à la base de données sous-jacente, même si le contrôle n’a pas perdu le focus.</span><span class="sxs-lookup"><span data-stu-id="1d7d2-106">One type of bindable property needs to notify every change to the database, for example with a check box control where every change needs to be sent through to the underlying database even though the control has not lost the focus.</span></span> <span data-ttu-id="1d7d2-107">Toutefois, les contrôles tels qu’une zone de liste ne veulent que la modification d’une propriété notifiée à la base de données lorsque le contrôle perd le focus, car l’utilisateur a peut-être modifié la sélection mise en surbrillance à l’aide des touches de direction avant de trouver le paramètre souhaité, afin que la notification de modification soit envoyée à la base de</span><span class="sxs-lookup"><span data-stu-id="1d7d2-107">However controls such as a listbox only wish to have the change of a property notified to the database when the control loses focus, as the user may have changed the highlighted selection with the arrow keys before finding the desired setting, to have the change notification sent to the database every time that the user hit the arrow key would be give unacceptable performance.</span></span> <span data-ttu-id="1d7d2-108">La nouvelle propriété de liaison immédiate permet à des propriétés pouvant être liées dans un formulaire d’avoir ce comportement spécifié, lorsque ce bit est défini, toutes les modifications sont notifiées.</span><span class="sxs-lookup"><span data-stu-id="1d7d2-108">The new immediate bind property allows individual bindable properties on a form to have this behavior specified, when this bit is set all changes will be notified.</span></span>

<span data-ttu-id="1d7d2-109">Le nouveau bit ImmediateBind est mappé au nouveau VARFLAG \_ FIMMEDIATEBIND (0x80) et aux bits FUNCFLAG \_ FIMMEDIATEBIND (0x80) dans les énumérations VARFLAGS et FUNCFLAGS de l’interface [ITypeInfo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) , ce qui permet d’inspecter les attributs des propriétés.</span><span class="sxs-lookup"><span data-stu-id="1d7d2-109">The new ImmediateBind bit maps through to the new VARFLAG\_FIMMEDIATEBIND (0x80) and the FUNCFLAG\_FIMMEDIATEBIND (0x80) bits in the VARFLAGS and FUNCFLAGS enumerations for the [ITypeInfo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interface allowing for the properties attributes to be inspected.</span></span>

 

 