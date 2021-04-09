---
title: Avantages de l’utilisation des extensions ADSI
description: La façon dont les méthodes d’extension sont implémentées dépend du writer d’extension.
ms.assetid: dbd1a203-b94c-4739-8c9d-aed1c9b43426
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27e80e6c095fcc02ca02c57b0987d1e6ed410ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028571"
---
# <a name="benefits-of-using-adsi-extensions"></a>Avantages de l’utilisation des extensions ADSI

La façon dont les méthodes d’extension sont implémentées dépend du writer d’extension. Un enregistreur d’extension peut même implémenter une méthode complètement en dehors de la portée du répertoire. Par exemple, un développeur de logiciels de sauvegarde et de restauration prévoit d’étendre un objet appelé **ordinateur**. Le développeur doit créer deux méthodes : la **sauvegarde** et la **restauration**. Ces méthodes fonctionnent à distance sur l’ordinateur physique sur lequel l’objet **ordinateur** de l’annuaire pointe. En agissant en tant qu’extension, le composant accède à l’infrastructure ADSI et est affiché par les clients ADSI en tant que partie intégrante de l’objet.

Les scénarios suivants décrivent les situations où la création d’une extension à ADSI est avantageuse :

-   Créez une extension pour intégrer un composant à l’objet d’annuaire. Comme il existe un objet **utilisateur** dans l’annuaire, un développeur de RH peut souhaiter créer une extension ADSI qui remplit d’autres données dans le répertoire lors de la création d’un **utilisateur** .
-   Créez une extension si un composant requiert une recherche dans le répertoire. Un composant peut exiger un répertoire comme point de départ pour une recherche. Par exemple, lors de la création d’une nouvelle application. Un objet d’application, **ToolApp**, peut être publié dans l’annuaire. Votre application peut prendre en charge les notifications d’État sur un regroupement de serveurs de messagerie. Vous décidez de faire de cette application une extension ADSI.

    À présent, un utilisateur peut rechercher toutes les instances de **ToolApp** dans le répertoire. Pour chaque objet retourné, l’utilisateur peut émettre un appel à **NotifyNow ()**. Une application ou une extension peut obtenir plus de données d’objet actuelles dans le répertoire et notifier chaque serveur de façon asynchrone.

-   Créez une extension comme une jonction entre les espaces de noms et les modèles de programmation. Par exemple, un ISV invente un nouveau modèle objet pour les services d’impression. L’objet **PrintQueue** est déjà défini dans l’annuaire. L’éditeur de logiciels indépendant peut créer une extension ADSI et l’associer à l’objet **PrintQueue** . Les utilisateurs ADSI peuvent effectuer une liaison à un objet **PrintQueue** et commencer à utiliser le modèle objet pour l’ISV. Du point de vue du client ADSI, ce point de jonction est transparent.
-   Créer une extension pour simplifier les tâches. De nombreuses tâches du répertoire peuvent être effectuées en recherchant et en définissant plusieurs attributs dans un ou plusieurs objets. En créant une fonction unique pour manipuler plusieurs attributs, elle simplifie le développement des enregistreurs d’applications et de scripts.

Pour les clients ADSI, les extensions enrichissent l’environnement de programmation ADSI de plusieurs façons :

-   Les développeurs qui créent des clients ADSI n’ont pas besoin d’apprendre un nouveau modèle de programmation. Les extensions font partie d’ADSI. Ils utilisent le même paradigme pour la recherche, la manipulation des données et la sécurisation des objets.
-   Les administrateurs peuvent gérer les applications associées utilisant des annuaires à l’aide d’extensions.
-   Les consommateurs d’extensions peuvent afficher un objet et une extension ADSI sous la forme d’un objet intégré.
-   Les composants existants peuvent être intégrés à ADSI, ce qui permet aux extensions de tirer parti des investissements existants et de créer une synergie entre les composants.

Les extensions ADSI ont été conçues avec les objectifs suivants :

-   Facile à implémenter. Avec les technologies Microsoft actuelles existantes, Microsoft Visual C++ système de développement et le Active Template Library, une extension peut être créée rapidement.
-   Les clients affichent un IDispatch. Du point de vue des writers de script et Automation, les méthodes et propriétés d’extension sont fusionnées de manière transparente dans un objet ADSI.
-   Indépendante. Les rédacteurs d’extensions peuvent étendre ADSI indépendamment sans connaissance préalable des extensions existantes.

Prenons ce scénario : un développeur d’entreprise ou un ISV doit développer un programme de sauvegarde. Cette application de sauvegarde permet à un administrateur de sauvegarder tous les ordinateurs d’une unité d’organisation. Avec une extension ADSI, le script suivant est possible.


```VB
Dim ou
On Error Resume Next
Set ou = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
If Err.Number<>0 Then
    MsgBox("An error has occurred.")
    Err.Clear
    Set ou = Nothing
    Exit Sub
End If

ou.Filter = Array("computer")

For each comp in ou
   Debug.Print comp.Get("networkAddress")
   Debug.Print comp.LastBackUp
   comp.BackUpNow
Next
```



**LastBackUp** est une propriété et **BackUpNOW** est une méthode fournie par l’enregistreur d’extensions. Le code illustre les avantages pour les consommateurs d’extension et les fournisseurs. Le générateur d’extensions n’a pas besoin de créer une nouvelle façon de filtrer, de rechercher et d’accéder au répertoire. Le consommateur de l’extension n’a pas besoin de réapprendre un nouveau paradigme de programmation. Les nouvelles méthodes et propriétés fournies par le writer d’extension sont affichées dans le cadre de l’interface ADSI.

 

 




