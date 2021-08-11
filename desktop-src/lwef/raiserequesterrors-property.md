---
title: Propriété RaiseRequestErrors
description: Propriété RaiseRequestErrors
ms.assetid: 60eb4478-526e-492a-8fb3-d1e54eff9868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081a47eef17378c24df5bdbcb0f5141b0dece45ec9933f289d0b3da9193793d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246612"
---
# <a name="raiserequesterrors-property"></a>Propriété RaiseRequestErrors

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit une valeur indiquant si les erreurs pour les demandes sont déclenchées.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent * * *. RaiseRequestErrors* *  \[  =  *booléen*\]



| Partie      | Description                                                                                                                                                                                            |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Valeur booléenne qui détermine si les erreurs dans les demandes sont déclenchées.<br/> **True**    (valeur par défaut) les erreurs de requête sont générées. <br/> **Valeur false**     Les erreurs de demande ne sont pas déclenchées.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Cette propriété vous permet de déterminer si le serveur génère des erreurs qui se produisent avec les méthodes qui prennent en charge les objets de [**requête**](/windows/desktop/lwef/the-request-object) . Par exemple, si vous spécifiez un nom d’animation qui n’existe pas dans une méthode [**Play**](play-method.md), le serveur génère une erreur (en affichant le message d’erreur), sauf si vous affectez la valeur **false** à cette propriété.

Il peut être utile pour les langages de programmation qui ne fournissent pas de récupération lorsqu’une erreur est générée. Toutefois, soyez vigilant lorsque vous affectez à cette propriété la **valeur false**, car il peut être plus difficile de trouver des erreurs dans votre code.

 

