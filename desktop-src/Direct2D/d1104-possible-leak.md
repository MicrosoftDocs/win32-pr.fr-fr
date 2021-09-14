---
title: Fuite de D1104 possible
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: La fabrique a été libérée mais l’interface créée à partir de celle-ci est toujours active. Bien qu’il soit possible de libérer des ressources après avoir libéré la fabrique, cette condition peut indiquer une fuite de mémoire.
keywords:
- D1104 de fuite possible
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b6629a0da2b89e13feebc33fe5742e3459fc082b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114090"
---
# <a name="d1104-possible-leak"></a>D1104 : fuite possible

La \[ *fabrique* \] de fabrique a été libérée mais l' \[ *interface* \] d’interface créée à partir de celle-ci est toujours active. Bien qu’il soit possible de libérer des ressources après avoir libéré la fabrique, cette condition peut indiquer une fuite de mémoire.

## <a name="placeholders"></a>Espaces réservés

<dl> <dt>

<span id="factory"></span><span id="FACTORY"></span>*fabrique*
</dt> <dd>

Adresse de la fabrique qui a été libérée.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interface*
</dt> <dd>

Adresse de l’interface qui a été créée sur la *fabrique*.

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| Niveau d’erreur | Information |



 

## <a name="possible-causes"></a>Causes possibles

La fabrique a été libérée mais l’interface créée à partir de celle-ci est toujours active.

 

 




