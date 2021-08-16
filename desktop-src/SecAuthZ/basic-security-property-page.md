---
description: Page de démarrage de la feuille de propriétés affichée par la fonction EditSecurity. Vous pouvez également utiliser la fonction CreateSecurityPage pour créer une page de propriétés de sécurité de base à insérer dans votre propre feuille de propriétés.
ms.assetid: 6623fe7e-e91d-49c7-9ad0-7791c178d12b
title: Page de propriétés sécurité de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8628b0b096e24a3a7baef94f5ab9913c2cd89825bb15bf6b19d18cd81d1033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783706"
---
# <a name="basic-security-property-page"></a>Page de propriétés sécurité de base

La page de propriétés sécurité de base est la page de démarrage de la feuille de propriétés affichée par la fonction [**EditSecurity**](/windows/desktop/api/Aclui/nf-aclui-editsecurity) . Vous pouvez également utiliser la fonction [**CreateSecurityPage**](/windows/desktop/api/Aclui/nf-aclui-createsecuritypage) pour créer une page de propriétés de sécurité de base à insérer dans votre propre feuille de propriétés.

La page de propriétés [affiche la liste](trustees.md) des destinataires nommés dans les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) de la [*liste de contrôle d’accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) de l’objet (DACL). La page contient également une liste des droits d’accès pris en charge par l’objet. Lorsque l’utilisateur sélectionne un nom dans la liste des tiers de confiance, les cases à cocher en regard de chaque droit d’accès indiquent les droits qui sont autorisés ou refusés pour ce tiers de confiance. L’utilisateur peut ensuite activer ou désactiver les cases à cocher pour modifier les droits d’accès du tiers de confiance. L’utilisateur peut également ajouter ou supprimer des utilisateurs de confiance dans la liste.

La page de propriétés sécurité de base ne peut pas afficher des entrées de contrôle d’accès complexes, telles que des [ACE spécifiques à un objet ou des](object-specific-aces.md)informations d’héritage ACE. Pour permettre à l’utilisateur d’afficher ou de modifier ces informations, vous pouvez inclure un bouton **avancé** dans la page sécurité de base. L’utilisateur peut cliquer sur le bouton **avancé** pour afficher une [feuille de propriétés de sécurité avancée](advanced-security-property-sheet.md). Cette feuille de propriétés a des pages de propriétés qui permettent à l’utilisateur de modifier la [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL) de l’objet, de modifier le propriétaire de l’objet ou d’effectuer une modification avancée de la liste DACL de l’objet. Pour afficher le bouton **avancé** , définissez l' \_ indicateur si avancé dans la structure d’informations de l' [**\_ objet \_ si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) retournée par votre implémentation de [**ISecurityInformation :: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .

Vous pouvez utiliser le membre **pszPageTitle** de la structure d’informations de l' [**\_ objet \_ si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) pour spécifier le titre de la page de propriétés de sécurité de base. Le titre par défaut est **sécurité**.

 

 
