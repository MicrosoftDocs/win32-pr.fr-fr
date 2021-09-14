---
description: le WiLstPrd.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. L’exemple de script se connecte à un objet installer et énumère les produits inscrits et les informations produit.
ms.assetid: 13615dc2-ebc7-4536-9dd8-9bb1dbf3cfaf
title: Répertorier les produits, les propriétés, les fonctionnalités et les composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20d2f563efad42108f763b909e7a1118e255dcb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011958"
---
# <a name="list-products-properties-features-and-components"></a>Répertorier les produits, les propriétés, les fonctionnalités et les composants

le WiLstPrd.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). L’exemple de script se connecte à un objet [**installer**](installer-object.md) et énumère les produits inscrits et les informations produit.

Cet exemple illustre l’utilisation de :

-   [**Propriété ProductInfo**](installer-productinfo.md)
-   [**Propriété ProductState (objet installer)**](installer-productstate-property.md)
-   [**Products, propriété**](installer-products.md)
-   [**Fonctionnalités, propriété**](installer-features.md)
-   [**Propriété FeatureParent**](installer-featureparent.md)
-   [**Propriété FeatureState**](installer-featurestate.md)
-   [**Components, propriété**](installer-components.md)
-   [**Propriété ComponentClients**](installer-componentclients.md)
-   [**Propriété ComponentPath**](installer-componentpath.md)
-   [**Méthode LastErrorRecord**](installer-lasterrorrecord.md)
-   [**Méthode RegistryValue**](installer-registryvalue.md) de l' [ **objet installer**](installer-object.md)

vous aurez besoin de la version CScript.exe ou WScript.exe de Windows Script Host pour utiliser cet exemple. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une ligne de commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ chemin d’accès au fichier \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiLstPrd.vbs \[ options de nom de produit \] \[\]**

Spécifiez le nom du produit non sensible à la casse ou le GUID de l’ID de produit du produit installé ou publié. Si aucun produit ou option n’est spécifié, le programme d’installation répertorie tous les produits installés ou publiés sur le système.

Notez que ces options ne sont pas des commutateurs. par conséquent, vous ne devez pas les faire précéder d’une barre oblique (/) sur la ligne de commande. Les options suivantes peuvent être combinées en concaténant les lettres. Par exemple, « PC » pour répertorier les propriétés des produits et les composants installés.



| Option               | Description                                                                                                                           |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| aucune option spécifiée | Répertorie les propriétés des produits.                                                                                                        |
| p                    | Répertorie les propriétés des produits.                                                                                                        |
| f                    | Répertorier les fonctionnalités, les parents des fonctionnalités et les États d’installation des produits                                                                 |
| c                    | Répertorie les composants installés du produit.                                                                                              |
| d                    | répertoriez la valeur sous **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ SharedDlls** pour les fichiers de clé du composant des produits. |



 

pour plus d’informations, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md) pour des exemples de scripts supplémentaires. pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows hôte de Script, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).

 

 



