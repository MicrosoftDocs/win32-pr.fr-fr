---
title: /Oi (commutateur)
description: Les commutateurs/OI et/OIC indiquent au compilateur MIDL d’utiliser une méthode de marshaling entièrement interprétée. Le commutateur/Oicf fournit des améliorations de performances supplémentaires.
ms.assetid: cf597a45-410f-4098-850b-240c6ebce23b
keywords:
- Option de commutateur/OI
topic_type:
- apiref
api_name:
- /Oi
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1671b16640d3f3214f10138e50a2ac08b6114674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104198883"
---
# <a name="oi-switch"></a>/Oi (commutateur)

Les commutateurs **/OI** et **/OIC** indiquent au compilateur MIDL d’utiliser une méthode de marshaling entièrement interprétée. Le commutateur **/Oicf** fournit des améliorations de performances supplémentaires.

``` syntax
midl /{Oi | Oic | Oif | Oicf}
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*OI* 
</dt> <dd>

Spécifie la méthode entièrement interprétée pour le marshaling du code stub passé entre le client et le serveur.

> [!Note]  
> Ce commutateur est obsolète. Il est recommandé d’utiliser le commutateur **/Oicf** à la place.

 

</dd> <dt>

*Oic* 
</dt> <dd>

Spécifie la méthode de proxy non codée du marshaling qui fournit toutes les fonctionnalités de **/OI** et réduit également la taille du code stub client pour les interfaces d’objet.

> [!Note]  
> Ce commutateur est obsolète. Il est recommandé d’utiliser le commutateur **/Oicf** à la place.

 

</dd> <dt>

*Interfaces de Oicf* 
</dt> <dd>

Spécifie la méthode de proxy sans code du marshaling qui inclut toutes les fonctionnalités fournies par **/OI** et **/OIC** , mais utilise un nouvel interpréteur (chaînes de format rapide) qui offre de meilleures performances que **/OI** ou **/OIC**. Ce commutateur comprend des améliorations récentes de RPC et est recommandé pour les scénarios RPC modernes.

</dd> </dl>

## <a name="remarks"></a>Notes

Veuillez noter les restrictions liées aux plateformes de prise en charge.

Le compilateur MIDL 3,0 fournit deux méthodes pour marshaler du code : entièrement interprété ( **/OI**, **/OIC** et **/Oicf**) et en mode mixte ( [**/OS**](-os.md)). À compter de la version 6.0.359 de MIDL, le compilateur MIDL génère des stubs **/Oicf** Â  [**/Robust**](-robust.md) par défaut. Certaines fonctionnalités du langage ne sont pas prises en charge dans certains modes. Dans ce cas, le compilateur bascule automatiquement vers le mode approprié et émet un avertissement.

Si les performances constituent un problème, la méthode en mode mixte ( [**/OS**](-os.md)) peut être la meilleure approche. Dans ce mode, le compilateur choisit de marshaler certains paramètres inline dans les stubs générés. Bien que cela entraîne une plus grande taille de stub, elle offre des performances accrues.

La méthode entièrement interprétée marshale les données complètement hors connexion. Cela réduit considérablement la taille du code stub, mais entraîne une baisse des performances. En outre, avec la méthode entièrement interprétée, il existe une limite de 16 paramètres pour chaque procédure. Toute procédure contenant plus de 16 paramètres sera automatiquement traitée en mode [**/OS**](-os.md) . Parmi les modes interprétés, **/Oicf** offre les meilleures performances et **/OI** offre la meilleure compatibilité descendante.

Vous pouvez utiliser l’option **/OIF** si votre application utilise des fonctionnalités MIDL qui ont été introduites avec MIDL 3,0, telles que les attributs du \[ [**\_ marshaleur de câble**](wire-marshal.md) et du \] \[ [**\_ Marshal d’utilisateur**](user-marshal.md) \] . Si votre application utilise des [canaux](/windows/desktop/Rpc/pipes) , vous devez utiliser l’option **/OIF** ; Si vous spécifiez un autre mode, le compilateur MIDL passe à **/OIF**.

Pour affiner la façon dont votre code stub est marshalé, Microsoft RPC fournit un attribut d' \[ [**optimisation**](optimize.md) ACF \] . Cet attribut est utilisé en tant qu’attribut d’interface ou d’opération pour sélectionner le mode de marshaling pour des interfaces individuelles ou pour des opérations individuelles.

### <a name="calling-conventions"></a>Conventions d’appel

Les stubs générés par le compilateur MIDL dans la méthode interprétée à l’aide des commutateurs **/OI**, **/OIC** ou **/OIF** doivent être compilés comme une procédure stdcall ou cdecl pendant la compilation C. Une convention d’appel PASCAL ou fastcall ne fonctionnera pas. En outre, le stub du serveur doit être compilé comme StdCall.

## <a name="examples"></a>Exemples

**MIDL/OI nom de fichier. idl**

**MIDL/OIC NomFichier. idl**

**MIDL/OIF NomFichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**/Robust**](-robust.md)
</dt> <dt>

[**/non \_ robuste**](-no-robust.md)
</dt> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/OS**](-os.md)
</dt> <dt>

[**requêtes**](optimize.md)
</dt> <dt>

[**/non \_ format \_ opt**](-no-format-opt.md)
</dt> </dl>

 

 