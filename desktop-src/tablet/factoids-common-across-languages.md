---
description: Un certain nombre de Factoids décrivent les entrées communes à tous les moduleurs de langage et n’ont pas besoin d’avoir des formats différents pour des langues différentes. Le tableau suivant répertorie les Factoids qui sont communs à tous les langages.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Factoids commun dans plusieurs langues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 407a82c72367d0123414f72b083b1d3416cfc958
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294023"
---
# <a name="factoids-common-across-languages"></a>Factoids commun dans plusieurs langues

Un certain nombre de Factoids décrivent les entrées communes à tous les moduleurs de langage et n’ont pas besoin d’avoir des formats différents pour des langues différentes. Le tableau suivant répertorie les Factoids qui sont communs à tous les langages.




| Factoid | Définition | Exemples | 
|---------|------------|----------|
| <strong>Caractères</strong> | Définit le décalage pour un chiffre unique. Le module de reconnaissance est biaisé pour retourner uniquement des chiffres quand ce Factoid est défini.<br /> | 0-9<br /> | 
| <strong>E-mail</strong> | Définit le décalage pour une adresse de messagerie.<br /> | someone@example.com<br /> | 
| <strong>Web</strong> | Définit le décalage pour différents formats d’URL.<br /><blockquote>[!Note]<br />Les paramètres par défaut pour le module de reconnaissance incluent le Factoid <strong>Web</strong> . Pour cette raison, vous ne pouvez pas remarquer une différence importante entre le Factoid <strong>Web</strong> et le paramètre par défaut. Toutefois, le Factoid <strong>Web</strong> permet d’éliminer les espaces entre les mots d’une URL.</blockquote><br /> | http : \\ Microsoft.net<br /> https://microsoft.us/<br /> https : \\ www.Microsoft.au \<br />https://microsoft.com<br /> www.microsoft_world. com<br /> www.microsoft.us \<br /> http : \\www.microsoft.com\myfile.htm<br /> http : \\www.microsoft.com\myfile.html<br /> http : \\ www. Microsoft. com\myfile.asp<br /> http : \\ www.Microsoft.uk<br /> http : \\ www.Microsoft.info<br /> www.microsoft.biz<br /> | 
| <strong>Par défaut</strong> | Retourne le module de reconnaissance à ses paramètres par défaut.<br /> | Le paramètre par défaut pour Factoids pour les langues occidentales comprend le dictionnaire système, le dictionnaire de l’utilisateur, les différents signes de ponctuation et le <strong>Web</strong> et le <strong>numéro</strong> Factoids.<br /> Le paramètre par défaut pour Factoids pour les langues d’Extrême-Orient comprend tous les caractères pris en charge par le module de reconnaissance.<br /> | 
| <strong>Aucun</strong> | Désactive tous les Factoids, les dictionnaires et le modèle de langue.<br /> | Ce Factoid doit être utilisé uniquement lorsque vous ne voulez pas que le module de reconnaissance utilise des règles grammaticales ou des dictionnaires, y compris le dictionnaire système. Ce Factoid est utile pour l’entrée de chaînes aléatoires, telles que les codes de produit. N’utilisez pas l’indicateur de forçage avec ce Factoid.<br /> | 




 

 

 




