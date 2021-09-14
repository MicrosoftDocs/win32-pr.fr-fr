---
description: la version de PATCHWIZ.DLL publiée avec Windows Installer&\# 160 ; 3.0 peut générer automatiquement des informations de séquencement de correctifs et ajouter à la Table MsiPatchSequence un nouveau correctif.
ms.assetid: 03e7eea6-1a37-4c86-a9da-109fbaf20728
title: Génération d’informations sur les séquences de correctifs (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff82166f33266a58cd3ef299b2546b04a94ebb14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021684"
---
# <a name="generating-patch-sequence-information-patchwizdll"></a>Génération d’informations sur les séquences de correctifs (PATCHWIZ.DLL)

la version de [PATCHWIZ.DLL](patchwiz-dll.md) publiée avec Windows Installer 3,0 peut générer automatiquement des informations de séquencement de correctifs et ajouter à la [Table MsiPatchSequence](msipatchsequence-table.md) un nouveau correctif.

Définissez la \_ \_ propriété de génération de données \_ de séquence désactivé sur 1 (un) dans la [table de propriétés](properties-table-patchwiz-dll-.md) du fichier. PCP pour empêcher la génération automatique des informations de séquencement de correctifs. Si cette propriété est absente, les informations sont automatiquement générées et ajoutées.

lorsque le [PATCHWIZ.DLL](patchwiz-dll.md) fourni avec Windows Installer 3,0 est utilisé pour générer automatiquement les informations de séquencement des correctifs, voici ce qui se produit :

-   Une nouvelle ligne est ajoutée à la [table MsiPatchSequence](msipatchsequence-table.md) pour chaque code de produit d’une image cible qui est indiquée dans la [table TargetImages](targetimages-table-patchwiz-dll-.md).
-   Les valeurs ajoutées à la colonne PatchFamily dans les nouvelles lignes correspondent aux codes de produit cibles des images cibles qui sont répertoriées dans la [table TargetImages](targetimages-table-patchwiz-dll-.md).
-   Les valeurs ajoutées aux colonnes de séquence dans les nouvelles lignes sont générées à l’aide de la version de produit la plus élevée ciblée par le correctif et de l’heure UTC à laquelle le correctif est généré. Le numéro de séquence est <Product Minor Version> . <Build Major Number> . <horodatage 1>. <horodatage 2>.
    -   Le premier champ correspond à la version du produit de la version la plus récente du produit ciblée par le correctif.
    -   Le deuxième champ est le numéro principal de la version la plus récente du produit ciblé par le correctif.

    Les deux champs d’horodatage pour l’horodatage de 32 bits, qui est nécessaire pour compter les secondes en temps universel coordonné (UTC, Universal Time Coordinated).
    > [!Note]  
    > Les versions du produit ont le format suivant : <Product Major Version> .. <Product Minor Version> <Build Major Number> . <Build Minor Number> et un produit avec un numéro de version 2.1.0.0 est une version supérieure à celle d’un produit avec le numéro de version 1.2.0.0

     

-   L’attribut msidbPatchSequenceSupersedeEarlier est entré dans la colonne attribut des nouvelles lignes générées pour les service packs (SP) ou les correctifs de mise à niveau mineure. L’attribut msidbPatchSequenceSupersedeEarlier n’est pas ajouté à un correctif QFE ou à une mise à jour de petite taille.
    > [!Note]  
    > Un Service Pack (SP) doit contenir les correctifs de tous les correctifs qui ont été publiés avant celui-ci. Toutefois, si un auteur de correctif définit la \_ propriété de remplacement des données de séquence \_ sur 0 (zéro) ou 1 (un) dans le fichier. PCP, la colonne attributs de toutes les lignes de la table MsiPatchSequence est définie sur la valeur spécifiée pour le remplacement des données de séquence \_ \_ . Les auteurs de correctifs qui requièrent davantage de contrôle doivent créer manuellement la colonne d’attributs.

     

Si vous incluez une [table PatchSequence](patchsequence-table--patchwiz-dll-.md) dans le fichier. PCP, la \_ \_ propriété de génération de données de séquence \_ désactivée est ignorée et les informations fournies dans la table PatchSequence peuvent être ajoutées à la [table MsiPatchSequence](msipatchsequence-table.md) du correctif.

 

 



