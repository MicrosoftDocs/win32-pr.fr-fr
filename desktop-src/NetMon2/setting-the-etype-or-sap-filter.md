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
# <a name="setting-the-etype-or-sap-filter"></a>Définition du filtre ETYPE ou SAP

La définition de la partie ETYPE ou SAP du filtre de capture est la première étape du processus de création de filtre de capture.

Dans l’exemple suivant, le filtre de capture est défini pour récupérer uniquement le trafic IPX :


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



Les valeurs SAP et ETYPE sont généralement disponibles dans les RFC. Les valeurs SAP et ETYPE peuvent être dans un tableau.

 

 



