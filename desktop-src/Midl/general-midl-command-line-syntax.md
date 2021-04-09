---
title: Syntaxe générale de la ligne de commande MIDL
description: Le compilateur MIDL traite un fichier IDL et un fichier de configuration d’application facultatif (ACF) pour générer un jeu de fichiers de sortie.
ms.assetid: 1906b374-d0d1-4ec8-9a00-c5228b4c29ca
keywords:
- Référence de ligne de commande MIDL, syntaxe générale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14baa145c7be03467a24bd4298cf2f502d93b6ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840729"
---
# <a name="general-midl-command-line-syntax"></a>Syntaxe générale de la ligne de commande MIDL

Le compilateur MIDL traite un fichier IDL et un fichier de configuration d’application facultatif (ACF) pour générer un jeu de fichiers de sortie. Les attributs spécifiés dans la liste d’attributs d’interface du fichier IDL déterminent si le compilateur génère des fichiers sources pour une interface RPC ou pour une interface OLE personnalisée.

## <a name="switch-options"></a>Options de commutateur

``` syntax
     midl [command-line-switch [switch-options]] filename
    
```

<dl> <dt>

<span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*commutateur de ligne de commande*
</dt> <dd>

Spécifie les commutateurs de ligne de commande du compilateur MIDL. Les commutateurs peuvent apparaître dans n’importe quelle séquence.

</dd> <dt>

<span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*options du commutateur*
</dt> <dd>

Spécifie les options associées à chaque commutateur. Les options valides sont décrites dans l’entrée de référence pour chaque commutateur du compilateur MIDL.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extension*
</dt> <dd>

Spécifie le nom du fichier IDL. Ce fichier a généralement l’extension. idl, mais il peut en avoir un autre ou aucun.

</dd> </dl>

## <a name="remarks"></a>Notes

Les listes suivantes affichent les noms par défaut des fichiers générés pour un fichier IDL nommé Name. idl. Vous pouvez utiliser des commutateurs de ligne de commande pour remplacer ces noms par défaut. Notez que le nom du fichier IDL peut avoir une extension autre que. idl ou aucune extension.

Par défaut (autrement dit, si la liste d’attributs d’interface ne contient pas l' [**objet**](object.md) ou l’attribut [**local**](local.md) ), le compilateur génère les fichiers suivants pour une [interface RPC](files-generated-for-an-rpc-interface.md):

-   Stub client (nom \_ c. c)
-   Serveur stub (nom \_ s. c)
-   Fichier d’en-tête (Name. h)

Lorsque l’attribut d' [**objet**](object.md) apparaît dans la liste attribut d’interface, le compilateur génère les fichiers suivants pour une interface com :

-   Fichier de proxy d’interface (nom \_ p. c)
-   Fichier d’en-tête d’interface (Name. h)
-   Fichier UUID de l’interface (nom \_ I. c)

Lorsque l’attribut [**local**](local.md) apparaît dans la liste d’attributs de l’interface, le compilateur génère uniquement le fichier d’en-tête d’interface, Name. h.

Le compilateur MIDL fourni avec Microsoft RPC appelle le préprocesseur C en fonction des besoins pour traiter le fichier IDL. Il n’appelle pas automatiquement le compilateur C pour compiler les fichiers générés.

> [!Note]  
> Le compilateur MIDL fourni avec Microsoft RPC utilise une syntaxe de ligne de commande différente de celle du compilateur IDL DCE.

 

Le compilateur MIDL bascule [**/env**](-env.md), [**/Server**](-server.md), [**/sstub**](-sstub.md)et [**/out**](-out.md) sur le fichier stub du serveur.

À compter de la version 6.0.359 de MIDL, l’option de ligne de commande par défaut pour le compilateur MIDL est [**/Oicf**](-oi.md)Â  [**/Robust**](-robust.md). Pour désactiver/Robust, spécifiez l’option [**/non \_ robustesse**](-no-robust.md) .

## <a name="the-header-file"></a>Fichier d’en-tête

Le fichier d’en-tête contient les définitions de tous les types de données et opérations déclarés dans le fichier IDL. Le fichier d’en-tête doit être inclus par tous les modules d’application qui appellent les opérations définies, implémentent les opérations définies ou manipulent les types définis.

Le compilateur MIDL bascule [**/header**](-header.md) et [**/out**](-out.md) sur le fichier d’en-tête.

 

 




