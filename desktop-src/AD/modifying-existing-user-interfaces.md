---
title: Modification des interfaces utilisateur existantes
description: Le volet des résultats du composant logiciel enfichable MMC Active Directory utilisateurs et ordinateurs affiche plusieurs colonnes de données d’attribut pour les objets d’un conteneur, comme les attributs nom et description.
ms.assetid: 55f4ae82-c380-42a9-beba-047ffd0131eb
ms.tgt_platform: multiple
keywords:
- Modification des interfaces utilisateur existantes Active Directory
- AD du composant logiciel enfichable utilisateurs et ordinateurs, modification de l’affichage
- Composant logiciel enfichable utilisateurs et ordinateurs Active Directory, ajout de colonnes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf6ef4743009086ae19148c42a8addc5974e4ac833cdad8eee675fdce76a5f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025867"
---
# <a name="modifying-existing-user-interfaces"></a>Modification des interfaces utilisateur existantes

Le volet des résultats du composant logiciel enfichable MMC Active Directory utilisateurs et ordinateurs affiche plusieurs colonnes de données d’attribut pour les objets d’un conteneur, comme les attributs **nom** et **Description** . Le composant logiciel enfichable permet à l’utilisateur d’ajouter et de supprimer les colonnes affichées dans le volet de résultats du composant logiciel enfichable.

Pour modifier l’affichage, l’utilisateur utilise le menu déroulant **vue** et sélectionne **Ajouter/supprimer des colonnes**. Dans la boîte de dialogue **Ajouter/supprimer des colonnes** , il existe une liste de colonnes dans laquelle l’utilisateur peut choisir de s’afficher dans le volet des résultats.

le composant logiciel enfichable MMC utilisateurs et ordinateurs Active Directory inclus avec Windows server 2003, Édition Standard, Windows server 2003, Êdition Entreprise et Windows server 2003, Datacenter Edition, offre la possibilité de modifier la liste des colonnes qui peuvent être affichées dans le volet de résultats du composant logiciel enfichable pour un conteneur. cette fonctionnalité existe uniquement si le composant logiciel enfichable est ciblé sur une forêt avec le schéma Windows Server 2003.

Pour ajouter une colonne à la liste, ajoutez une valeur à l’attribut **extraColumns** du spécificateur d’affichage du type d’objet auquel l’attribut est associé. L’attribut **extraColumns** est un attribut de chaîne à valeurs multiples dans lequel chaque chaîne est au format suivant.


```C++

<ldapdisplayname>,<column header>,<default visibility>,<width>,<unused>

```



Le tableau suivant répertorie le contenu de ces valeurs.



| Valeur                        | Description                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| « &lt; ldapDisplayName &gt; »    | Contient une chaîne qui représente le **ldapDisplayName** de l’attribut.                                                         |
| « &lt; en-tête de colonne &gt; »      | Contient une chaîne qui représente le texte affiché dans l’en-tête de la colonne.                                                  |
| " &lt; visibilité par défaut &gt; " | Contient une valeur numérique égale à 0 si l’attribut est masqué par défaut ou égal à 1 si l’attribut est visible par défaut.               |
| « &lt; Width &gt; »              | Contient la largeur de la colonne en pixels. Si cette valeur est égale à-1, la largeur de la colonne est définie sur la largeur de l’en-tête de colonne. |
| « &lt; inutilisé &gt; »             | Inutilisé. Doit être zéro.                                                                                                               |



 

Par exemple, pour ajouter une colonne qui affichera le nom canonique des objets d’une unité d’organisation, une valeur pour l’attribut **canonicalName** est ajoutée à l’attribut **extraColumns** de l’objet **OrganizationalUnit-Display** dans le conteneur Spécificateurs d’affichage. La chaîne ajoutée à l’attribut **extraColumns** de l’objet **OrganizationalUnit-Display** se présente comme suit.


```C++
canonicalName,Canonical Name,0,150,0
```



La boîte de dialogue **Ajouter/supprimer des colonnes** affiche uniquement les colonnes contenues dans l’attribut **extraColumns** de l’objet **displaySpecifier** du type de conteneur affiché. Si l’attribut **extraColumns** ne contient aucune valeur, la boîte de dialogue **Ajouter/supprimer des colonnes** affiche un ensemble fixe de colonnes. Une copie de l’ensemble fixe de colonnes est contenue dans l’attribut **extraColumns** de l’objet d' **affichage par défaut** .

Pour ajouter une ou plusieurs colonnes à la liste des colonnes d’un objet spécifique, vous devez copier toutes les valeurs **extraColumns** de l’objet d' **affichage par défaut** vers l’objet cible, puis ajouter les colonnes personnalisées. Si vous spécifiez l’attribut **extraColumns** sur une classe donnée, cette classe utilisera ces colonnes et ne les fusionnera pas avec les colonnes spécifiées dans la classe d' **affichage par défaut** . Par conséquent, les modifications apportées à la classe d' **affichage par défaut** n’auront aucun effet sur cet objet.

Pour afficher une colonne personnalisée pour tous les types de conteneurs qui n’ont pas de colonnes personnalisées inscrites, ajoutez une valeur pour la colonne à l’attribut **extraColumns** de l’objet d' **affichage par défaut** .

 

 




