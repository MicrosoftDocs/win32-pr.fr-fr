---
title: Ressource User-Defined
description: Une instruction de définition de ressource définie par l’utilisateur définit une ressource qui contient des données spécifiques à l’application.
ms.assetid: b1cfec71-5733-4900-97f6-c1cbb350c728
keywords:
- ressource définie par l’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b383b7c4d1f9acfc4ce6c9db24efa77f3bfed943c1f299186d42a1facee2b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472616"
---
# <a name="user-defined-resource"></a>Ressource User-Defined

Une instruction de définition de ressource définie par l’utilisateur définit une ressource qui contient des données spécifiques à l’application. Les données peuvent avoir n’importe quel format et peuvent être définies en tant que contenu d’un fichier donné (si le paramètre de *nom de fichier* est donné) ou sous la forme d’une série de nombres et de chaînes (si le bloc de *données brutes* est spécifié).

``` syntax
nameID typeID filename
```

Le *nom de fichier spécifie* le nom d’un fichier contenant les données binaires de la ressource. Le contenu du fichier est inclus en tant que ressource. RC n’interprète pas les données binaires de quelque manière que ce soit. Il incombe au programmeur de s’assurer que les données sont correctement alignées pour l’architecture de l’ordinateur cible.

Une ressource définie par l’utilisateur peut également être entièrement définie dans le script de ressources à l’aide de la syntaxe suivante :

``` syntax
nameID typeID  {  raw-data  }
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nom unique ou entier 16 bits non signé qui identifie la ressource.

</dd> <dt>

<span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*typeID*
</dt> <dd>

Nom unique ou entier 16 bits non signé qui identifie le type de ressource. Si un nombre est donné, il doit être supérieur à 255. Les nombres 1 à 255 sont réservés pour les types de ressources redéfinis existants et futurs.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extension*
</dt> <dd>

Nom du fichier qui contient les données de ressource. Le paramètre doit être un nom de fichier valide ; il doit s’agir d’un chemin d’accès complet si le fichier ne se trouve pas dans le répertoire de travail actuel.

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*données brutes*
</dt> <dd>

Données brutes constituées d’un ou plusieurs entiers ou chaînes de caractères. Les entiers peuvent être spécifiés au format décimal, octal ou hexadécimal. pour être compatible avec les Windows 16 bits, les entiers sont stockés en tant que valeurs de mot. Vous pouvez stocker un entier comme valeur DWORD en qualifiant l’entier avec le suffixe « L ».

Les chaînes sont placées entre guillemets. RC n’ajoute pas automatiquement un caractère null de fin à une chaîne. Chaque chaîne est une séquence de caractères ANSI spécifiée, sauf si vous la qualifiez comme une chaîne de caractères larges avec le préfixe « L ».

Le bloc de données commence sur une limite **DWORD** et RC n’effectue aucun remplissage ou alignement des données dans le bloc de *données brutes* . Il incombe au programmeur de garantir l’alignement correct des données dans le bloc.

</dd> </dl>

## <a name="example"></a> Exemple

L’exemple suivant illustre plusieurs instructions définies par l’utilisateur :

``` syntax
array   MYRES   data.res
14      300     custom.res
18 MYRES2
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

 

 




