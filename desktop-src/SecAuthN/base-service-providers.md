---
description: Ces fournisseurs de services fournissent les fonctionnalités de base des cartes à puce.
ms.assetid: 1d887c4c-095c-4e1e-8b9a-7761acda2cbf
title: Fournisseurs de services de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25dfa6c190e7a09ed4dfceafb983878906e8e3b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952215"
---
# <a name="base-service-providers"></a>Fournisseurs de services de base

Ces [*fournisseurs de services*](/windows/desktop/SecGloss/c-gly) fournissent les fonctionnalités de base des [*cartes à puce*](/windows/desktop/SecGloss/s-gly) . Ils peuvent être utilisés pour accéder à une seule capacité de carte à puce, ou leurs interfaces COM peuvent être combinées pour fournir plusieurs fonctionnalités au sein d’un fournisseur de services unique. Ces fournisseurs de services sont les blocs de construction pour le développement de fonctionnalités supplémentaires pour d’autres fournisseurs de services.

Les tâches suivantes peuvent être effectuées par les interfaces de fournisseur de services de base fournies par le kit de développement logiciel (SDK) de carte à puce.



| Tâche                                                                                                                   | Interfaces du fournisseur de services de base         | DLL      |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------|----------|
| Connectez-vous à une carte à puce, implémentez des transactions, fermez les connexions, et ainsi de suite.                                         | [**ISCard**](iscard.md)                 | SCardSSP |
| Conserver une commande APDU et [*répondre aux APDU*](/windows/desktop/SecGloss/r-gly).          | [**ISCardCmd**](iscardcmd.md)           | SCardSSP |
| Interrogez la [*base de données de la carte à puce*](/windows/desktop/SecGloss/s-gly). | [**ISCardDatabase**](iscarddatabase.md) | SCardSSP |
| Localisez une carte à puce ou un lecteur.                                                                                         | [**ISCardLocate**](iscardlocate.md)     | SCardSSP |
| Générez une commande ISO7816-4 APDU.                                                                                       | [**ISCardISO7816**](iscardiso7816.md)   | SCardSSP |
| Encapsulez une mémoire tampon IStream en utilisant des types compatibles Visual Basic.                                                         | [**IByteBuffer**](ibytebuffer.md)       | SCardSSP |



 

La procédure suivante illustre une utilisation classique de ces interfaces de fournisseur de services de base. Dans cet exemple, les interfaces [**ISCard**](iscard.md), [**ISCardISO7816**](iscardiso7816.md)et [**ISCardCmd**](iscardcmd.md) sont utilisées pour exécuter une transaction.

**Pour effectuer une transaction**

1.  Créez une instance pour toutes les interfaces du fournisseur de services de base nécessaires (par exemple, [**ISCard**](iscard.md), [**ISCardISO7816**](iscardiso7816.md)et [**ISCardCmd**](iscardcmd.md)).
2.  Connectez-vous à une carte à puce particulière à l’aide des méthodes de l’interface [**ISCard**](iscard.md) .
3.  À l’aide de [**ISCardISO7816**](iscardiso7816.md) et d’un objet [**ISCardCmd**](iscardcmd.md) , générez une commande ISO 7816-4 en appelant la méthode **ISCardISO7816** . La commande est contenue dans **ISCardCmd** en tant que commande APDU.
4.  Effectuez une transaction avec la carte en appelant la méthode de transaction [**ISCard**](iscard.md) et en passant l’objet [**ISCardCmd**](iscardcmd.md) créé. Une fois la transaction terminée, les résultats sont stockés dans la **ISCardCmd** de réponse APDU.
5.  Interprétez les [**ISCardCmd**](iscardcmd.md) de réponse APDU et répétez la procédure.
6.  Libère toutes les interfaces lorsque les opérations sont terminées.

Pour plus d’informations sur la commande APDU générée dans les dll, consultez [génération d’une commande APDU ISO7816-4](building-an-iso7816-4-apdu-command.md).

 

 
