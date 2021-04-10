---
description: La définition de la partie ETYPE ou SAP du filtre de capture est la première étape du processus de création de filtre de capture.
ms.assetid: 0a22f74b-5bb1-43df-a70a-9f30195177ea
title: Définition du filtre ETYPE ou SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee117e992968265be5a973f3f4017832ee6ca0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951260"
---
# <a name="setting-the-etype-or-sap-filter"></a><span data-ttu-id="977db-103">Définition du filtre ETYPE ou SAP</span><span class="sxs-lookup"><span data-stu-id="977db-103">Setting the Etype or SAP Filter</span></span>

<span data-ttu-id="977db-104">La définition de la partie ETYPE ou SAP du filtre de capture est la première étape du processus de création de filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="977db-104">Setting the Etype or SAP portion of the capture filter is the first step in the capture filter creation process.</span></span>

<span data-ttu-id="977db-105">Dans l’exemple suivant, le filtre de capture est défini pour récupérer uniquement le trafic IPX :</span><span class="sxs-lookup"><span data-stu-id="977db-105">In the following example, the capture filter is set to only retrieve IPX traffic:</span></span>


```C++
BYTE Sap[]   = { 0x10, 0xE0 };
WORD Etype[] = { 0x8137 }; 

rc = SetNPPEtypeSapFilter(m_hBlob, 
     2,      //  nSaps,
     1,      //  nEtypes,
     &Sap,   //  LPBYTE lpSapTable,
     &Etype, //  LPWORD lpEtypeTable,
     0,      //  DWORD  FilterFlags,
     NULL
);
```



<span data-ttu-id="977db-106">Les valeurs SAP et ETYPE sont généralement disponibles dans les RFC.</span><span class="sxs-lookup"><span data-stu-id="977db-106">SAP and Etype values are usually available in RFCs.</span></span> <span data-ttu-id="977db-107">Les valeurs SAP et ETYPE peuvent être dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="977db-107">Both SAP and Etype values can be in an array.</span></span>

 

 



