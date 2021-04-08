---
title: Unload, méthode
description: Unload, méthode
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d19f5f29647ff01b5a52bd8978694aaef1c43a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725916"
---
# <a name="unload-method"></a><span data-ttu-id="cd870-103">Unload, méthode</span><span class="sxs-lookup"><span data-stu-id="cd870-103">Unload Method</span></span>

<span data-ttu-id="cd870-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cd870-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="cd870-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="cd870-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="cd870-106">Décharge les données de caractères pour le caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="cd870-106">Unloads the character data for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="cd870-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="cd870-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="cd870-108">*agent ***. Characters. Unload "*** CharacterID \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="cd870-108">*agent ***.Characters.Unload "*** CharacterID\*\*\*"*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd870-109">Notes</span><span class="sxs-lookup"><span data-stu-id="cd870-109">Remarks</span></span>

<span data-ttu-id="cd870-110">Utilisez cette méthode lorsque vous n’avez plus besoin d’un caractère, pour libérer de la mémoire utilisée pour stocker des informations sur le caractère.</span><span class="sxs-lookup"><span data-stu-id="cd870-110">Use this method when you no longer need a character, to free up memory used to store information about the character.</span></span> <span data-ttu-id="cd870-111">Si vous accédez de nouveau au caractère, utilisez la méthode [**Load**](load-method.md) .</span><span class="sxs-lookup"><span data-stu-id="cd870-111">If you access the character again, use the [**Load**](load-method.md) method.</span></span>

<span data-ttu-id="cd870-112">Cette méthode ne retourne pas d’objet de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="cd870-112">This method does not return a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 