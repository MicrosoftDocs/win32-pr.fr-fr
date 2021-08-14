---
description: L’outil SetReg définit la valeur des clés de Registre qui contrôlent le comportement du processus de vérification du certificat Authenticode.
ms.assetid: 6c456a59-ee6c-420d-b075-7de8bd2fd8ff
title: SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5267aa140cad713e550ddf8afd0281d489bdd90ac0b26a7f7a4781240ecac24c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900299"
---
# <a name="setreg"></a>SetReg

L’outil SetReg définit la valeur des clés de Registre qui contrôlent le comportement du processus de vérification du certificat Authenticode. Ces clés sont appelées clés d’état de publication de logiciels. À l’issue de l’action demandée, l’outil affiche l’état actuel des clés de l’état de publication de logiciels.

**SetReg** \[ *Options* \] \[ *Choix \#* {**true** \| **false**}\]

l’outil Set Registry est fourni uniquement avec le kit de développement logiciel (SDK) .NET Framework version 1,0 et. 1,1, que vous pouvez télécharger à partir du [centre de téléchargement Microsoft](https://www.microsoft.com/download/details.aspx?id=16217).

## <a name="options"></a>Options

Les options peuvent être l’une des valeurs suivantes. Les options indiquées dans le tableau suivant peuvent être utilisées uniquement avec Internet Explorer 4,0 ou version ultérieure.



| Option | Description                                                                                                                                            |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-q** | Supprimez l’affichage des valeurs de clé de l’état de publication de logiciels après l’exécution de l’action demandée par SetReg. Les valeurs sont affichées par défaut. |
| **-?** | Répertorie la syntaxe de commande et les options.                                                                                                                       |



 

## <a name="choice-"></a>Sélectionnée \#

*Choix \#* doit avoir l’une des valeurs suivantes.



| Choix | Description                                                                                                                       | Résultat                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------|-----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **1**  | Approuver la racine de test                                                                                                               | Cette valeur est ignorée. **Windows XP/2000 :** Si la **valeur est true**, approuve une racine de test. Cela équivaut à exécuter « RegEdit wvtston. reg » dans Internet Explorer 3. *x*.<br/> La valeur par défaut est **false**. Tout fichier signé avec une racine de test ne sera pas vérifié, sauf si cet indicateur a la valeur **true**. notez que ce comportement a changé avec Windows xp avec Service pack 1 (SP1), car Windows XP avec sp1 ignore cette valeur.<br/> <br/> |
| **2**  | Utiliser la date d’expiration sur les certificats                                                                                               | Si la **valeur est true**, vérifie la date d’expiration du certificat. Pour ignorer les dates d’expiration, définissez cet indicateur sur **false**. La valeur par défaut est **true**.                                                                                                                                                                                                                                                                                                       |
| **3**  | Vérifier la [ *liste de révocation*](../secgloss/c-gly.md) | Si la **valeur est true**, le contrôle de révocation est effectué. Pour contourner la vérification de la révocation, définissez cet indicateur sur **false**. La valeur par défaut est **true**. **Internet Explorer 3. *x*:** la valeur par défaut est **false**.<br/>                                                                                                                                                                                                                                               |
| **4**  | Serveur de révocation hors connexion OK (individuel)<br/>                                                                              | Si la **valeur est true**, autorise l’approbation hors connexion pour les certificats individuels. La valeur par défaut est **false**.                                                                                                                                                                                                                                                                                                                                                 |
| **5**  | Serveur de révocation hors connexion OK (commercial)<br/>                                                                              | Si la **valeur est true**, autorise l’approbation hors connexion pour les certificats commerciaux. La valeur par défaut est **true**.                                                                                                                                                                                                                                                                                                                                                  |
| **6**  | Serveur de révocation hors connexion Java OK (individuel)<br/>                                                                         | Si la **valeur est true**, autorise l’approbation hors connexion pour les certificats individuels et n’affiche pas l’interface utilisateur pour les certificats incorrects. La valeur par défaut est **false**.                                                                                                                                                                                                                                                                                    |
| **7**  | Serveur de révocation hors connexion Java OK (commercial)<br/>                                                                         | Si la **valeur est true**, autorise l’approbation hors connexion pour les certificats commerciaux et n’affiche pas l’interface utilisateur pour les certificats incorrects. La valeur par défaut est **true**.                                                                                                                                                                                                                                                                                     |
| **8**  | Rendre les objets signés de la version 1 qui ne sont plus valides                                                                                     | Si la **valeur est true**, les objets signés de la version 1 ne sont plus valides. La valeur par défaut est **false**.                                                                                                                                                                                                                                                                                                                                                      |
| **9**  | Vérifier la liste de révocation du serveur d’horodatage                                                                                | Si la **valeur est true**, effectue la vérification de la révocation sur le certificat du serveur d’horodatage. La valeur par défaut est **false**. **Internet Explorer 3. *x*:** cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                                                            |
| **10** | Seuls les éléments de confiance trouvés dans la base de données d’approbation                                                                                      | Si la **valeur est true**, autorise les téléchargements à partir des serveurs de publication contenus dans la base de données de confiance personnelle. La valeur par défaut est **false**. **Internet Explorer 3. *x*:** cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                                             |



 

 

 
