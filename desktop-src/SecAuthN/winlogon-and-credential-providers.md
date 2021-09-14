---
description: est le module Windows qui effectue une ouverture de session interactive pour une ouverture de session. Le comportement de Winlogon peut être personnalisé en implémentant et en inscrivant un fournisseur d’informations d’identification.
ms.assetid: 6721367b-e200-4297-897b-4772226203b0
title: Winlogon et fournisseurs d’informations d’identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce72e533f7cee6bc89bc2f995b94b7881448734d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096190"
---
# <a name="winlogon-and-credential-providers"></a>Winlogon et fournisseurs d’informations d’identification

[*Winlogon*](../secgloss/w-gly.md) est le module Windows qui effectue une ouverture de session interactive pour une [*ouverture de session*](../secgloss/l-gly.md). Le comportement de Winlogon peut être personnalisé en implémentant et en inscrivant un fournisseur d’informations d’identification.

Pour plus d’informations sur l’implémentation d’un fournisseur d’informations d’identification, consultez les rubriques suivantes.



| Rubrique                                                                                                           | Description                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [expérience de connexion Windows basée sur le fournisseur d’informations d’identification](https://go.microsoft.com/fwlink/?LinkId=717287)<br/> | Présentation de Winlogon et de l’architecture du fournisseur d’informations d’identification et d’un exemple de fournisseur d’informations d’identification.<br/> |
| [Interfaces Shell](../shell/samples-usingthumbnailproviders.md)<br/>                                                                | Référence de l’interface du fournisseur d’informations d’identification.<br/>                                                    |
| [Fournisseurs d’informations d’identification dans Windows 10](credential-providers-in-windows.md)<br/>                            | Fournisseurs d’informations d’identification tiers et fournisseurs d’informations d’identification système dans Windows 10.<br/>             |



 

pour obtenir un exemple d’implémentation de fournisseur d’informations d’identification, consultez l’exemple situé dans le répertoire d’installation de SDK Windows sous \\ exemples de \\ sécurité \\ CredentialProvider.

**Windows Server 2003 et Windows XP :** Les fournisseurs d’informations d’identification ne sont pas pris en charge. Pour plus d’informations sur la personnalisation de Winlogon, consultez [Winlogon et Gina](winlogon-and-gina.md).

 

 
