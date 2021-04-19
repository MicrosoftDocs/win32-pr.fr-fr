---
title: delete cache
description: Vide l’intégralité du cache d’URL ou supprime les entrées en fonction de l’URL spécifiée.
ms.assetid: 499ce0f9-01db-4648-89f7-1ecafd25a805
keywords:
- supprimer le cache HTTP
topic_type:
- apiref
api_name:
- delete cache
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f963d12812140d11923460235ef780a621ba3db5
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "106512706"
---
# <a name="delete-cache"></a>delete cache

Vide l’intégralité du cache d’URL ou supprime les entrées en fonction de l’URL spécifiée.

``` syntax
delete cache [url=]string [[recursive=]{yes|no}]
 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>**\[URL = \] * * * chaîne*
</dt> <dd>

Obligatoire. Spécifie l’URL complète.

</dd> </dl>

<dl> <dt>

<span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[récursif = \] {Oui \| non}**
</dt> <dd>

Si c’est le cas, supprime toutes les entrées sous l’URL spécifiée.

</dd> </dl>

## <a name="examples"></a>Exemples

**supprimer l’URL du cache = https://www.contoso.com:80/myresource/ recursive = Oui**

 

 




