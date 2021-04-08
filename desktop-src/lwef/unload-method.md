---
title: Unload, méthode
description: Unload, méthode
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d19f5f29647ff01b5a52bd8978694aaef1c43a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725916"
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

*agent ***. Characters. Unload "*** CharacterID * * *"**

</dd> </dl>

## <a name="remarks"></a>Notes

Utilisez cette méthode lorsque vous n’avez plus besoin d’un caractère, pour libérer de la mémoire utilisée pour stocker des informations sur le caractère. Si vous accédez de nouveau au caractère, utilisez la méthode [**Load**](load-method.md) .

Cette méthode ne retourne pas d’objet de [**requête**](/windows/desktop/lwef/the-request-object) .

 

 