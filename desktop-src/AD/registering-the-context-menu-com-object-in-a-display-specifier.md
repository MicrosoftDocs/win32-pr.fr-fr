---
title: Inscription de l’objet COM du menu contextuel dans un spécificateur d’affichage
description: Cette rubrique présente les clés de Registre qui doivent être modifiées pour inscrire un objet COM de menu contextuel.
ms.assetid: 389bc249-4849-4763-9d1b-b35598a51050
ms.tgt_platform: multiple
keywords:
- Inscription de l’objet COM du menu contextuel dans un spécificateur d’affichage
- objet COM du menu contextuel, inscription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae30c1a60a1a0bc5a8ec388a3578ab13829c95
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104030987"
---
# <a name="registering-the-context-menu-com-object-in-a-display-specifier"></a>Inscription de l’objet COM du menu contextuel dans un spécificateur d’affichage

Lorsque vous utilisez COM pour créer une DLL d’extension de menu contextuel pour un service d’annuaire Active Directory, l’extension doit être inscrite auprès du Registre Windows et Active Directory Domain Services pour notifier les Active Directory composants logiciels enfichables MMC d’administration et le shell Windows de l’extension.

## <a name="registering-in-the-windows-registry"></a>Inscription dans le Registre Windows

Comme tous les serveurs COM, une extension de menu contextuel doit être inscrite dans le registre. L’extension est inscrite sous la clé suivante.

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

*<clsid>* représentation sous forme de chaîne du CLSID telle qu’elle est produite par la fonction [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) . Sous la *<clsid>* clé, il existe une clé **InprocServer32** qui identifie l’objet en tant que serveur in-proc 32 bits. Sous la clé **InprocServer32** , l’emplacement de la dll est spécifié dans la valeur par défaut et le modèle de thread est spécifié dans la valeur **ThreadingModel** . Toutes les extensions de menu contextuel doivent utiliser le modèle de thread « Apartment ».

## <a name="registering-with-active-directory-domain-services"></a>Inscription avec Active Directory Domain Services

L’inscription de l’extension du menu contextuel est spécifique à un paramètre régional. Si l’extension du menu contextuel s’applique à tous les paramètres régionaux, elle doit être inscrite dans l’objet [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) de la classe d’objet dans tous les sous-conteneurs de paramètres régionaux dans le conteneur de spécificateurs d’affichage. Si l’extension de menu contextuel est localisée pour un certain nombre de paramètres régionaux, elle doit être inscrite dans l’objet **displaySpecifier** dans le sous-conteneur de ces paramètres régionaux. Pour plus d’informations sur le conteneur et les paramètres régionaux des spécificateurs d’affichage, consultez [spécificateurs d’affichage](display-specifiers.md) et [conteneur DisplaySpecifiers](displayspecifiers-container.md).

Il existe deux attributs de spécificateur d’affichage sous lesquels un élément d’extension de menu contextuel peut être inscrit. Il s’agit de [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) et [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu).

L’attribut [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) identifie les menus contextuels d’administration à afficher dans Active Directory composants logiciels enfichables d’administration. Le menu contextuel s’affiche lorsque l’utilisateur affiche le menu contextuel pour les objets de la classe appropriée dans l’un des composants logiciels enfichables MMC d’administration de Active Directory.

L’attribut [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) identifie les menus contextuels de l’utilisateur final à afficher dans le shell Windows. Le menu contextuel s’affiche lorsque l’utilisateur consulte le menu contextuel des objets de la classe appropriée dans l’Explorateur Windows. À partir de Windows Server 2003, l’interpréteur de commandes Windows n’affiche plus d’objets de Active Directory Domain Services.

Tous ces attributs sont à valeurs multiples.

Lors de l’inscription d’une extension de menu contextuel, les valeurs des attributs [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) et [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) requièrent le format suivant.


```C++
<order number>,<clsid>
```



« &lt; Order Number &gt; » est un nombre non signé qui représente la position de l’élément dans le menu contextuel. Lorsqu’un menu contextuel s’affiche, les valeurs sont triées à l’aide d’une comparaison de la valeur « &lt; Order Number » de chaque valeur &gt; . Si plusieurs valeurs ont le même « numéro de &lt; commande &gt; », ces extensions de menu contextuel sont chargées dans l’ordre dans lequel elles sont lues à partir du serveur de Active Directory. Si possible, utilisez un « numéro d’ordre » non existant &lt; &gt; , autrement dit un « numéro d’ordre » qui n’a pas été utilisé par d’autres valeurs de la propriété. Il n’existe pas de position de départ prescrite et les espaces sont autorisés dans la &lt; séquence « Order Number &gt; ».

Le &lt; CLSID &gt; est la représentation sous forme de chaîne du CLSID tel qu’il a été généré par la fonction [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

Dans le shell Windows, les éléments de menu contextuel à sélection multiple sont pris en charge. Dans ce cas, l’extension du menu contextuel est appelée pour chaque objet sélectionné. Dans Active Directory composants logiciels enfichables d’administration, les éléments d’extension de menu contextuel à sélection multiple sont également pris en charge. Dans ce cas, la structure [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) contient une structure [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) pour chaque objet d’annuaire sélectionné.

> [!IMPORTANT]
> Pour le shell Windows, les informations relatives au spécificateur d’affichage sont récupérées à l’ouverture de session de l’utilisateur et mises en cache pour la session de l’utilisateur. Pour les composants logiciels enfichables d’administration, les données du spécificateur d’affichage sont récupérées lorsque le composant logiciel enfichable est chargé et mis en cache pour la durée du processus. Pour le shell Windows, cela signifie que les modifications apportées aux spécificateurs d’affichage prennent effet une fois qu’un utilisateur se déconnecte puis de nouveau. Pour les composants logiciels enfichables d’administration, les modifications prennent effet lors du rechargement du composant logiciel enfichable ou de la console, autrement dit, si vous démarrez une nouvelle instance du fichier de console ou d’une nouvelle instance de Mmc.exe et que vous ajoutez le composant logiciel enfichable, les données du spécificateur d’affichage les plus récentes sont récupérées.

 

Pour plus d’informations et pour obtenir un exemple de code sur la façon d’implémenter une extension de menu contextuel, consultez [l’exemple de code pour l’implémentation de l’objet com du menu contextuel](example-code-for-implementation-of-the-context-menu-com-object.md).

 

 