---
description: La définition de la partie ETYPE ou SAP du filtre de capture est la première étape du processus de création de filtre de capture.
ms.assetid: 0a22f74b-5bb1-43df-a70a-9f30195177ea
title: Définition du filtre ETYPE ou SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abac637594debf03ca9f82c79382ababc4c696d79d5351b2d0be0a3e5b4ffa8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363164"
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

 

 



