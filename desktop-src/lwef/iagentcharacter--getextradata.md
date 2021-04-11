---
title: IAgentCharacter GetExtraData
description: IAgentCharacter GetExtraData
ms.assetid: 83f69bae-0ae3-45c5-ba0d-71610993da60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea854479ab85630abc3d110c9c193716ddedd004
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100821"
---
# <a name="iagentcharactergetextradata"></a><span data-ttu-id="c6c3d-103">IAgentCharacter::GetExtraData</span><span class="sxs-lookup"><span data-stu-id="c6c3d-103">IAgentCharacter::GetExtraData</span></span>

<span data-ttu-id="c6c3d-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c6c3d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetExtraData(
   BSTR * pbszExtraData   // address of buffer for additional character data
); 
```

<span data-ttu-id="c6c3d-105">Récupère des données supplémentaires stockées dans le cadre du caractère.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-105">Retrieves additional data stored as part of the character.</span></span>

-   <span data-ttu-id="c6c3d-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c6c3d-107"><span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*</span><span class="sxs-lookup"><span data-stu-id="c6c3d-107"><span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*</span></span>
</dt> <dd>

<span data-ttu-id="c6c3d-108">Adresse d’un BSTR qui reçoit la valeur des données supplémentaires pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-108">The address of a BSTR that receives the value of the additional data for the character.</span></span> <span data-ttu-id="c6c3d-109">Les données supplémentaires d’un caractère sont définies lorsqu’elles sont compilées avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-109">A character's additional data is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="c6c3d-110">Un développeur de caractères peut fournir cette chaîne en modifiant le. Fichier ACD pour un caractère.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-110">A character developer can supply this string by editing the .ACD file for a character.</span></span> <span data-ttu-id="c6c3d-111">Le paramètre est facultatif et ne peut pas être fourni pour tous les caractères, ni être défini ou modifié au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-111">The setting is optional and may not be supplied for all characters, nor can the data be defined or changed at run time.</span></span> <span data-ttu-id="c6c3d-112">En outre, la signification des données fournies est définie par le développeur de caractères.</span><span class="sxs-lookup"><span data-stu-id="c6c3d-112">In addition, the meaning of the data supplied is defined by the character developer.</span></span>

</dd> </dl>

 

 




