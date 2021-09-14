---
title: Services de texte Active Accessibility
description: Cette section décrit les interfaces des services de texte Active Accessibility.
ms.assetid: 8bbc647f-1687-45b8-8b63-a6ea45a0a721
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe9fdb4d9d9972f93db780d274b39e587e51c03b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010725"
---
# <a name="active-accessibility-text-services"></a>Services de texte Active Accessibility

Cette section décrit les interfaces des services de texte Active Accessibility.

> [!Note]  
> Active Accessibility Text services est déconseillé. pour plus d’informations sur l’entrée de texte avancée et les technologies de langage naturel, consultez [Microsoft Windows text Services Framework](../tsf/text-services-framework.md) .

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique                                                     | Description                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IAccServerDocMgr**](/windows/desktop/api/msaatext/nn-msaatext-iaccserverdocmgr)   | Expose des méthodes qui rendent des documents accessibles aux applications clientes.                              |
| [**IAccClientDocMgr**](/windows/desktop/api/msaatext/nn-msaatext-iaccclientdocmgr)   | Expose des méthodes pour que les applications clientes récupèrent des documents.                                      |
| [**IAccDictionary**](/windows/desktop/api/msaatext/nn-msaatext-iaccdictionary)       | Expose des méthodes pour la manipulation de chaînes.                                                            |
| [**ICoCreateLocally**](/windows/desktop/api/msaatext/nn-msaatext-icocreatelocally)   | Expose une méthode qui permet à une application cliente de créer un objet d’assistance dans le contexte du serveur. |
| [**ICoCreatedLocally**](/windows/desktop/api/msaatext/nn-msaatext-icocreatedlocally) | Expose une méthode pour retourner des informations sur un objet local.                                        |
| [**IVersionInfo**](/windows/desktop/api/msaatext/nn-msaatext-iversioninfo)           | Expose des méthodes qui fournissent des informations de version pour les éléments accessibles.                            |

## <a name="related-topics"></a>Rubriques connexes

[Active Accessibility les services d’interface utilisateur](active-accessibility-user-interface-services-dev-guide.md)