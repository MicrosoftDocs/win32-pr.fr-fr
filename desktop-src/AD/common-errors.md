---
title: Erreurs courantes (AD DS)
description: Le tableau suivant contient une liste d’erreurs courantes qui peuvent se produire en fonction de l’étendue du groupe imbriqué.
ms.assetid: 844d4280-a943-4906-b0c6-0c650ef9c114
ms.tgt_platform: multiple
keywords:
- Erreurs courantes AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c719aad39690932de51c58d0f8081a8c855980bd
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2019
ms.locfileid: "104462675"
---
# <a name="common-errors-ad-ds"></a>Erreurs courantes (AD DS)

Le tableau suivant contient une liste d’erreurs courantes qui peuvent se produire en fonction de l’étendue du groupe imbriqué.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>HRESULT</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x8007001F</td>
<td>Échec général. Cette erreur se produit si vous tentez d’effectuer les opérations suivantes :
<ul>
<li>Ajoutez un groupe de domaine local à un groupe global ou universel ou à un groupe de domaine local dans un autre domaine. Les groupes locaux de domaine peuvent uniquement être ajoutés en tant que membres à d’autres groupes locaux de domaine dans le même domaine.</li>
<li>Ajoutez un groupe universel à un groupe global. Les groupes universels peuvent être ajoutés à des groupes universels et locaux de domaine, mais pas à des groupes globaux.</li>
</ul></td>
</tr>
<tr class="even">
<td>0x8007202F</td>
<td><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>. Cette erreur se produit si vous tentez d’ajouter un groupe de sécurité à un autre groupe dans un domaine s’exécutant en mode mixte. Les groupes de sécurité ne peuvent pas être imbriqués en mode mixte ; les groupes de sécurité peuvent uniquement être imbriqués en mode natif.</td>
</tr>
</tbody>
</table>



 

 

 




