---
title: Unload, méthode
description: Unload, méthode
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74f274f758e34416cc73d82963fa21fbd93b14e7b6492c693f24b763081b49f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474497"
---
# <a name="unload-method"></a>Unload, méthode

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Décharge les données de caractères pour le caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères. Unload «**_CharacterID_*_»_*

</dd> </dl>

## <a name="remarks"></a>Remarques

Utilisez cette méthode lorsque vous n’avez plus besoin d’un caractère, pour libérer de la mémoire utilisée pour stocker des informations sur le caractère. Si vous accédez de nouveau au caractère, utilisez la méthode [**Load**](load-method.md) .

Cette méthode ne retourne pas d’objet de [**requête**](/windows/desktop/lwef/the-request-object) .

 

 