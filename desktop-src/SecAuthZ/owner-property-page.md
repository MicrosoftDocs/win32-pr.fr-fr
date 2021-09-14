---
description: L’éditeur de contrôle d’accès peut inclure une page de propriétés de propriétaire qui permet à l’utilisateur de modifier un propriétaire d’objets. Pour plus d’informations sur le propriétaire d’objets, consultez propriétaire d’un nouvel objet et appropriation d’objets en C++.
ms.assetid: b0c421db-450e-4030-98e9-e062202e482c
title: Page de propriétés propriétaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cee9d5c276071674ec274c9955a2e8c5cd5a856a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233430"
---
# <a name="owner-property-page"></a>Page de propriétés propriétaire

L’éditeur de contrôle d’accès peut inclure une page de propriétés de propriétaire qui permet à l’utilisateur de modifier le propriétaire d’un objet. Pour plus d’informations sur le propriétaire d’un objet, consultez [propriétaire d’un nouvel objet](owner-of-a-new-object.md) et [appropriation d’objets en C++](taking-object-ownership-in-c--.md).

La page de propriétés **propriétaire** se trouve dans la [feuille de propriétés de sécurité avancée](advanced-security-property-sheet.md) qui s’affiche lorsque l’utilisateur clique sur le bouton **avancé** de la [page de propriétés sécurité de base](basic-security-property-page.md). Pour inclure la page de propriétés **propriétaire** , définissez les \_ indicateurs SI avancé et si \_ modifier \_ le propriétaire dans la structure d’informations de l' [**\_ objet \_ si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) retournée par votre implémentation de [**ISecurityInformation :: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .

 

 
