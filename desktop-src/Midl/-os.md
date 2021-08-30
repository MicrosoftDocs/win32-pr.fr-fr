---
title: /OS (commutateur)
description: Le commutateur/OS spécifie la méthode en mode mixte pour marshaler le code stub passé entre le client et le serveur.
ms.assetid: dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb
keywords:
- MIDL du commutateur/OS
topic_type:
- apiref
api_name:
- /Os
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33b5e36984783369c96b331af55adac0c97eb8cc2688829d87f7b6d2cea0d7df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895939"
---
# <a name="os-switch"></a>/OS (commutateur)

Le commutateur **/OS** spécifie la méthode en mode mixte pour marshaler le code stub passé entre le client et le serveur.

``` syntax
midl /Os
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Remarques

Il y a des problèmes importants à prendre en compte avant de choisir la méthode de marshaling du code. Ces problèmes concernent la taille et les performances. Le compilateur MIDL fournit deux méthodes pour marshaler du code : mode mixte (**/OS**) et entièrement interprété ([**/OI**](-oi.md)). La méthode entièrement interprétée marshale les données complètement hors connexion. Cela réduit considérablement la taille du code stub, mais entraîne également une baisse des performances.

Utilisez le mode par défaut MIDL **/Oicf** /Robust pour tous les besoins autres que la compatibilité descendante. Ce mode est le mode sécurisé standard du compilateur MIDL. n’importe quel autre mode doit être utilisé uniquement après mûre réflexion sur l’implication de sécurité, la réalisation de ces futures extensions sera uniquement implémentée pour le mode par défaut. En mode mixte, le compilateur marshale certains paramètres inline dans les stubs générés. Bien que cela entraîne une plus grande taille de stub, elle peut également offrir des performances accrues.

MIDL offre une prise en charge complète des tableaux multidimensionnels et des pointeurs multidimensionnels uniquement en mode [**/Oicf**](-oi.md) . Dans les modes **/OS** et **/OI** , le compilateur prend en charge des cas simples, tels que des tableaux de taille fixe. L’utilisation de tableaux multidimensionnels en mode **/OS** ou **/OI** peut entraîner des paramètres qui ne sont pas correctement marshalés. Microsoft vous recommande d’utiliser le commutateur de ligne de commande **/Oicf** lorsque votre interface définit des paramètres qui sont des tableaux multidimensionnels ou des pointeurs de taille multidimensionnelle.

Pour définir plus précisément le niveau de gradation dans le mode de marshaling des données, cette version de RPC fournit un \[ [](optimize.md) \] attribut optimize. Cet attribut est utilisé comme attribut d’interface ou d’opération ACF pour sélectionner le mode de marshaling.

## <a name="examples"></a>Exemples

**MIDL/OS nom du fichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/OI**](-oi.md)
</dt> <dt>

[**requêtes**](optimize.md)
</dt> <dt>

[**/non \_ format \_ opt**](-no-format-opt.md)
</dt> </dl>

 

 




