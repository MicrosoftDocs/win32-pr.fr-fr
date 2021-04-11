---
title: IAgentNotifySink ActivateInputState
description: IAgentNotifySink ActivateInputState
ms.assetid: 2476e475-d80c-47e9-bb60-e0fca41becc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821f5943bb87f9c19a66125028604fa5d116a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197118"
---
# <a name="iagentnotifysinkactivateinputstate"></a><span data-ttu-id="36316-103">IAgentNotifySink::ActivateInputState</span><span class="sxs-lookup"><span data-stu-id="36316-103">IAgentNotifySink::ActivateInputState</span></span>

<span data-ttu-id="36316-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="36316-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ActivateInputState(
   long dwCharID,   // character ID
   long bActivated  // input activation flag
);                          
```

<span data-ttu-id="36316-105">Avertit une application cliente que l’état actif d’entrée d’un caractère a été modifié.</span><span class="sxs-lookup"><span data-stu-id="36316-105">Notifies a client application that a character's input active state changed.</span></span>

-   <span data-ttu-id="36316-106">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="36316-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="36316-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="36316-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="36316-108">Identificateur du caractère dont l’état d’activation de l’entrée a changé.</span><span class="sxs-lookup"><span data-stu-id="36316-108">Identifier of the character whose input activation state changed.</span></span>

</dd> <dt>

<span data-ttu-id="36316-109"><span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bActivated*</span><span class="sxs-lookup"><span data-stu-id="36316-109"><span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bActivated*</span></span>
</dt> <dd>

<span data-ttu-id="36316-110">Indicateur actif d’entrée.</span><span class="sxs-lookup"><span data-stu-id="36316-110">Input active flag.</span></span> <span data-ttu-id="36316-111">Cette valeur booléenne est **true** si le caractère référencé par *dwCharID* est devenu actif en entrée ; et **false** si le caractère a perdu son état actif d’entrée.</span><span class="sxs-lookup"><span data-stu-id="36316-111">This Boolean value is **True** if the character referred to by *dwCharID* became input active; and **False** if the character lost its input active state.</span></span>

</dd> </dl>

 

 




