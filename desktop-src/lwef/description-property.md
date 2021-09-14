---
title: Description, propriété (fonctionnalités héritées de l’environnement Windows)
description: Description, propriété
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4fb60b20a57f56a914c7e44ced957d91bf7085
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012378"
---
# <a name="description-property-legacy-windows-environment-features"></a>Description, propriété (fonctionnalités héritées de l’environnement Windows)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit une chaîne qui spécifie la description du caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent*. **Caractères («**_CharacterID_*_»)._* \[  =  *Chaîne* de description\]



| Partie     | Description                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| *string* | Valeur de chaîne correspondant à la description du caractère (dans le paramètre de langue actuel). |



 

</dd> </dl>

## <a name="remarks"></a>Notes

La **Description** d’un caractère peut dépendre du paramètre **LanguageID** du caractère. Le nom d’un caractère dans une langue peut être différent ou utiliser des caractères différents de ceux d’un autre langage. La **Description** par défaut du caractère pour une langue spécifique est définie lorsque le caractère est compilé à l’aide de l’éditeur de caractères Microsoft Agent.

> [!Note]  
> Le paramètre de propriété **Description** est facultatif et ne peut pas être fourni pour tous les caractères.

 

 

 




