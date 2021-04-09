---
description: Pour créer un fournisseur de classe WMI, vous devez inscrire l' \_ \_ instance Win32Provider qui représente votre fournisseur à l’aide d’une instance de \_ \_ ClassProviderRegistration.
ms.assetid: ed834969-47e9-47df-9db8-c805b2eb71da
ms.tgt_platform: multiple
title: Inscription d’un fournisseur de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc15893e654f96f8c4e476219389a1f8f2c464a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951579"
---
# <a name="registering-a-class-provider"></a>Inscription d’un fournisseur de classe

Pour créer un fournisseur de classe WMI, vous devez inscrire l’instance [**\_ \_ Win32Provider**](--win32provider.md) qui représente votre fournisseur à l’aide d’une instance de [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md). En tant qu’objet COM, votre fournisseur doit s’inscrire auprès du système d’exploitation et de WMI. La procédure suivante suppose que vous avez déjà implémenté le processus d’inscription, comme décrit dans [inscription d’un fournisseur](registering-a-provider.md). Si votre fournisseur stocke la plupart des données dans l’espace de stockage WMI et que celles-ci sont mises à jour uniquement lors de l’initialisation de WMI, enregistrez votre classe en tant que fournisseur de classe push. Si les données que vous fournissez changent fréquemment et sont récupérées dynamiquement par votre code à chaque demande de WMI, inscrivez votre fournisseur en tant que fournisseur de classe pull.

La procédure suivante décrit comment inscrire un fournisseur de classes push.

**Pour inscrire un fournisseur de classes Push**

-   Affectez la valeur 1 à la propriété **InteractionType** de l’instance [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) .

    La création d’une instance de [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) fait partie du processus d’inscription.

La procédure suivante décrit comment inscrire un fournisseur de classe pull.

**Pour inscrire un fournisseur de classe pull**

1.  Créez une instance de la classe [**\_ \_ Win32Provider**](--win32provider.md) qui décrit le fournisseur.
2.  Créez une instance de la classe [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) qui décrit l’ensemble des fonctionnalités du fournisseur.

    Dans l’instance [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) :

    1.  Définissez la propriété **InteractionType** pour indiquer si le fournisseur est un fournisseur push ou pull.
    2.  Baliser la classe avec les qualificateurs [**Dynamic**](standard-wmi-qualifiers.md) et [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) .

        Le qualificateur [**dynamique**](standard-wmi-qualifiers.md) indique que WMI doit utiliser un fournisseur pour récupérer les instances de classe. Le qualificateur du [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) spécifie le nom du fournisseur que WMI doit utiliser.

    3.  Définissez les propriétés **ResultSetQueries**, **ReferencedSetQueries** et **UnsupportedQueries** .

        Ces propriétés de requête décrivent des informations détaillées sur la classe prise en charge.

En plus de décrire les différentes méthodes prises en charge d’une classe, la classe [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) a également trois propriétés qui décrivent une série de requêtes. Lorsqu’elles sont utilisées ensemble, ces trois propriétés décrivent la plage entière des classes fournies par le fournisseur de classe. Chaque propriété de requête contient une instruction WQL SELECT, appelée « requête de schéma », pour spécifier les types de classes prises en charge. Les requêtes de schéma spécifient un nom de classe spécial appelé méta \_ Class. Le tableau suivant répertorie les propriétés de la requête.



| Propriété                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ResultSetQueries**     | Contient des informations sur le jeu de résultats fourni par le fournisseur. WMI utilise les informations pour déterminer s’il faut appeler le fournisseur pour répondre à une requête à partir d’une application. Cette propriété décrit soit l’ensemble de toutes les classes que le fournisseur peut fournir, soit un sur-ensemble des classes disponibles, mais jamais un sous-ensemble. WMI requiert qu’un fournisseur spécifie au moins une requête dans cette propriété.<br/> L’exemple suivant montre comment définir **ResultSetQueries** lorsqu’un fournisseur fournit une classe d’association qui référence la [**classe \_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .<br/> `SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"`<br/> L’exemple suivant montre comment spécifier une requête générale lorsqu’un fournisseur fournit des classes qui font référence à d’autres classes inconnues.<br/> `SELECT * FROM meta_class`<br/> L’exemple suivant montre comment définir **ResultSetQueries** lorsqu’un fournisseur fournit uniquement des sous-classes, mais pas la classe parente d’une classe donnée.<br/> `SELECT * FROM meta_class WHERE __Dynasty = "MyClass"`<br/> L’exemple suivant montre comment utiliser la propriété spéciale \_ \_ this et définir **ResultSetQueries** lorsqu’un fournisseur fournit toutes les classes et les sous-classes.<br/> `SELECT * FROM meta_class WHERE __this ISA "MyClass"`<br/> |
| **ReferencedSetQueries** | Détermine s’il faut ignorer le fournisseur dans les requêtes de schéma où des associations et des références sont demandées. Les fournisseurs qui peuvent fournir des classes d’association doivent inclure au moins une requête dans leur propriété **ReferencedSetQueries** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **UnsupportedQueries**   | Contient des informations sur le jeu de résultats qu’un fournisseur de classe ne fournit pas. WMI utilise cette propriété pour soustraire de l’ensemble de classes impliqué par **ResultSetQueries**. Par exemple, un fournisseur de classes peut spécifier la prise en charge de **ResultSetQueries** pour toutes les classes dérivées de MyClass et spécifier dans **UnsupportedQueries** un manque de prise en charge pour une classe dérivée particulière.<br/> Plus les informations qu’un fournisseur peuvent inscrire sur ses fonctionnalités de traitement des requêtes, plus l’exécution est rapide. La saisie d’une ou plusieurs requêtes dans la propriété **UnsupportedQueries** est une façon d’être spécifique et est particulièrement importante quand un fournisseur s’appuie sur une classe qu’il ne fournit pas. Quand une requête est effectuée pour une classe qui est listée dans une requête de la propriété **UnsupportedQueries** , WMI peut fournir la classe elle-même ou appeler un autre fournisseur pour le fournir.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

Comme WMI ne prend pas en charge la clause ou, vous devez créer une requête distincte pour chaque classe.

Les requêtes suivantes sont spécifiées dans **ResultSetQueries** lorsqu’un fournisseur de classes fournit MyClass1, MyClass2 et MyClass3.


```sql
SELECT * FROM meta_class WHERE __Class = "MyClass1"
SELECT * FROM meta_class WHERE __Class = "MyClass2"
SELECT * FROM meta_class WHERE __Class = "MyClass3"
```



Seuls les administrateurs peuvent inscrire ou supprimer un fournisseur en créant une instance de [**\_ \_ Win32Provider**](--win32provider.md) et [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md).

 

