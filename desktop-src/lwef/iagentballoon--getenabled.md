---
title: IAgentBalloon GetEnabled
description: IAgentBalloon GetEnabled
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d144374f690d295b80d0092add56439eb4e5fc9d546ba1f970ab99976cf2d7f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888390"
---
# <a name="iagentballoongetenabled"></a>IAgentBalloon :: GetEnabled

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetEnabled(
  long * pbEnabled  // address of variable for Enabled setting 
);                  // for word balloon
```

Récupère la valeur de la propriété [**Enabled**](enabled-property.md) pour une bulle de texte.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Adresse d’une variable qui reçoit la **valeur true** lorsque la bulle de texte est activée et **false** lorsqu’elle est désactivée.

</dd> </dl>

Le serveur Microsoft Agent affiche automatiquement le mot bulle pour la sortie parlée, sauf si elle est désactivée. La bulle de texte peut être désactivée pour un caractère de l’éditeur de caractères Microsoft agent ou (par l’utilisateur) pour tous les caractères de la feuille de propriétés de l’agent Microsoft. Si l’utilisateur désactive le mot-bulle, le client ne peut pas le restaurer.

 

 




