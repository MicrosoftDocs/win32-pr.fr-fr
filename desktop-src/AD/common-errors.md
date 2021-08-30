---
title: Erreurs courantes (AD DS)
description: Le tableau suivant contient une liste d’erreurs courantes qui peuvent se produire en fonction de l’étendue du groupe imbriqué.
ms.assetid: 844d4280-a943-4906-b0c6-0c650ef9c114
ms.tgt_platform: multiple
keywords:
- Erreurs courantes AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea02b1006cab476ca042a0026e66132af44cbaed
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469246"
---
# <a name="common-errors-ad-ds"></a>Erreurs courantes (AD DS)

Le tableau suivant contient une liste d’erreurs courantes qui peuvent se produire en fonction de l’étendue du groupe imbriqué.




| HRESULT | Description | 
|---------|-------------|
| 0x8007001F | Échec général. Cette erreur se produit si vous tentez d’effectuer les opérations suivantes :<ul><li>Ajoutez un groupe de domaine local à un groupe global ou universel ou à un groupe de domaine local dans un autre domaine. Les groupes locaux de domaine peuvent uniquement être ajoutés en tant que membres à d’autres groupes locaux de domaine dans le même domaine.</li><li>Ajoutez un groupe universel à un groupe global. Les groupes universels peuvent être ajoutés à des groupes universels et locaux de domaine, mais pas à des groupes globaux.</li></ul> | 
| 0x8007202F | <strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>. Cette erreur se produit si vous tentez d’ajouter un groupe de sécurité à un autre groupe dans un domaine s’exécutant en mode mixte. Les groupes de sécurité ne peuvent pas être imbriqués en mode mixte ; les groupes de sécurité peuvent uniquement être imbriqués en mode natif. | 




 

 

 




