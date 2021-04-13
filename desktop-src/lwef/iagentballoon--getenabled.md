---
title: IAgentBalloon GetEnabled
description: IAgentBalloon GetEnabled
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd78245534b942e7972066ec90179172f7b556c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311380"
---
# <a name="iagentballoongetenabled"></a><span data-ttu-id="4d2ca-103">IAgentBalloon :: GetEnabled</span><span class="sxs-lookup"><span data-stu-id="4d2ca-103">IAgentBalloon::GetEnabled</span></span>

<span data-ttu-id="4d2ca-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4d2ca-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
  long * pbEnabled  // address of variable for Enabled setting 
);                  // for word balloon
```

<span data-ttu-id="4d2ca-105">Récupère la valeur de la propriété [**Enabled**](enabled-property.md) pour une bulle de texte.</span><span class="sxs-lookup"><span data-stu-id="4d2ca-105">Retrieves the value of the [**Enabled**](enabled-property.md) property for a word balloon.</span></span>

-   <span data-ttu-id="4d2ca-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="4d2ca-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4d2ca-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="4d2ca-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="4d2ca-108">Adresse d’une variable qui reçoit la **valeur true** lorsque la bulle de texte est activée et **false** lorsqu’elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="4d2ca-108">The address of a variable that receives **True** when the word balloon is enabled and **False** when it is disabled.</span></span>

</dd> </dl>

<span data-ttu-id="4d2ca-109">Le serveur Microsoft Agent affiche automatiquement le mot bulle pour la sortie parlée, sauf si elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="4d2ca-109">The Microsoft Agent server automatically displays the word balloon for spoken output, unless it is disabled.</span></span> <span data-ttu-id="4d2ca-110">La bulle de texte peut être désactivée pour un caractère de l’éditeur de caractères Microsoft agent ou (par l’utilisateur) pour tous les caractères de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4d2ca-110">The word balloon can be disabled for a character in the Microsoft Agent Character Editor, or (by the user) for all characters in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="4d2ca-111">Si l’utilisateur désactive le mot-bulle, le client ne peut pas le restaurer.</span><span class="sxs-lookup"><span data-stu-id="4d2ca-111">If the user disables the word balloon, the client cannot restore it.</span></span>

 

 




