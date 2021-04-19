---
title: Liaison de données
description: Liaison de données
ms.assetid: 7fc5f036-8b36-4e0e-a257-173010fe127a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec6b8e66300834939a2b65fddefe947781350b0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106509879"
---
# <a name="databinding"></a>Liaison de données

Un nouvel attribut DataBinding a été ajouté pour permettre aux propriétés de faire la distinction entre les modifications de communication uniquement lorsque le focus quitte le contrôle ou pendant toutes les notifications de modification de propriété.

Le nouvel attribut, connu sous le nom de ImmediateBind, permet aux contrôles de différencier deux types différents de propriétés pouvant être liées. Un type de propriété pouvant être liée doit notifier chaque modification apportée à la base de données, par exemple avec un contrôle de case à cocher où chaque modification doit être envoyée à la base de données sous-jacente, même si le contrôle n’a pas perdu le focus. Toutefois, les contrôles tels qu’une zone de liste ne veulent que la modification d’une propriété notifiée à la base de données lorsque le contrôle perd le focus, car l’utilisateur a peut-être modifié la sélection mise en surbrillance à l’aide des touches de direction avant de trouver le paramètre souhaité, afin que la notification de modification soit envoyée à la base de La nouvelle propriété de liaison immédiate permet à des propriétés pouvant être liées dans un formulaire d’avoir ce comportement spécifié, lorsque ce bit est défini, toutes les modifications sont notifiées.

Le nouveau bit ImmediateBind est mappé au nouveau VARFLAG \_ FIMMEDIATEBIND (0x80) et aux bits FUNCFLAG \_ FIMMEDIATEBIND (0x80) dans les énumérations VARFLAGS et FUNCFLAGS de l’interface [ITypeInfo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) , ce qui permet d’inspecter les attributs des propriétés.

 

 