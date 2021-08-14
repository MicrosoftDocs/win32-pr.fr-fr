---
description: L’éditeur de contrôle d’accès peut inclure une page de propriétés d’audit qui permet à l’utilisateur d’afficher et de modifier les entrées de contrôle d’accès (ACE) dans une liste de contrôle d’accès système (SACL) d’objets. Pour plus d’informations sur les SACL, consultez listes de Access Control (ACL).
ms.assetid: 2a9152b7-c72d-4f03-bc3f-b75927fb4b6c
title: Page de propriétés d’audit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf116a9079c5b7b6dfeb7e6df57b45d6a0a2555c14de88a32fee4fadcdc6373
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784317"
---
# <a name="auditing-property-page"></a>Page de propriétés d’audit

L’éditeur de contrôle d’accès peut inclure une page de propriétés **d’audit** qui permet à l’utilisateur d’afficher et de modifier les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) dans la liste de contrôle d' [*accès système*](/windows/desktop/SecGloss/s-gly) (SACL) d’un objet. Pour plus d’informations sur les SACL, consultez [listes de Access Control](access-control-lists.md) (ACL).

**Pour afficher la page de propriétés audit**

-   Sur la [page de propriétés sécurité de base](basic-security-property-page.md), cliquez sur **avancé**. La page de propriétés **Auditing** se trouve dans la [feuille de propriétés de sécurité avancée](advanced-security-property-sheet.md).

Pour inclure la page de propriétés **d’audit** , définissez les indicateurs **si \_ avancé** et **si \_ modifier les \_ audits** dans la structure d’informations de l' [**\_ objet \_ si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) retournée par votre implémentation de [**ISecurityInformation :: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .

 

 
