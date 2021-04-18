---
title: Violation de Threading D1105
ms.assetid: 2c6cf90b-ce9e-4ea9-849d-22170f65ffb0
description: Une interface de location a été accessible simultanément à partir de plusieurs threads.
keywords:
- Violation de Threading D1105 Direct2D
topic_type:
- apiref
api_name:
- D1105 Threading Violation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe83baa32be8ae18948ae5a80e3e0b218cd4fa4a
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2021
ms.locfileid: "106529044"
---
# <a name="d1105-threading-violation"></a>D1105 : violation de thread

Une \[ *interface* \] d’interface de location de thread a été accessible simultanément à partir de plusieurs threads.

## <a name="placeholders"></a>Espaces réservés

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interface*
</dt> <dd>

Adresse de l’interface qui a été accessible par plusieurs threads.

</dd> </dl> 




 

## <a name="possible-causes"></a>Causes possibles

Utilisation d’une instance d’objet à partir de la même fabrique à thread unique à partir de deux threads différents.

 

 




