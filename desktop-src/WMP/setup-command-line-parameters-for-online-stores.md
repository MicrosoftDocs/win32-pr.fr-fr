---
title: Paramètres de ligne de commande d’installation pour les magasins en ligne
description: Paramètres de ligne de commande d’installation pour les magasins en ligne
ms.assetid: 26224d7c-ca12-43b9-9150-3d39bccb85d3
keywords:
- Lecteur Windows Media les magasins en ligne, paramètres de ligne de commande du programme d’installation
- magasins en ligne, paramètres de ligne de commande du programme d’installation
- tapez 1 magasins en ligne, paramètres de ligne de commande du programme d’installation
- tapez 2 magasins en ligne, paramètres de ligne de commande du programme d’installation
- paramètres de ligne de commande du programme d’installation
- Lecteur Windows Media les magasins en ligne, paramètres de ligne de commande
- magasins en ligne, paramètres de ligne de commande
- types 1 magasins en ligne, paramètres de ligne de commande
- types 2 magasins en ligne, paramètres de ligne de commande
- paramètres de ligne de commande
- Lecteur Windows Media les magasins en ligne, paramètres
- magasins en ligne, paramètres
- types 1 magasins en ligne, paramètres
- type 2 magasins en ligne, paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff77df581b2be4b2539772065e1aabef281a4c6c931ca115a4f6331063cf2414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569300"
---
# <a name="setup-command-line-parameters-for-online-stores"></a>Paramètres de ligne de commande d’installation pour les magasins en ligne

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

lors de l’installation de Lecteur Windows Media 10 ou Lecteur Windows Media 11 sur Windows XP, vous pouvez ajouter des paramètres de ligne de commande pour spécifier le premier magasin en ligne que l’utilisateur voit.

Syntaxe


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:serviceKey /ServiceInfo:documentPath /ServiceExtra:queryString"
```



Paramètres

DefaultService (obligatoire)

Nom de la clé du magasin en ligne. Cette valeur doit correspondre au nom de clé dans l’attribut de **clé** de l’élément **ServiceInfo** du document serviceInfo.

ServiceInfo (obligatoire)

Le chemin d’accès complet à un document ServiceInfo installé sur l’ordinateur de l’utilisateur.

ServiceExtra (facultatif)

une chaîne de requête qui Lecteur Windows Media 10 sera ajoutée à l’URL du document ServiceInfo lorsqu’il récupère le document en ligne.

## <a name="remarks"></a>Notes

pour plus d’informations sur la redistribution de Lecteur Windows Media logiciel à votre application, consultez [redistribution de Lecteur Windows Media logiciel](redistributing-windows-media-player-software.md).

lorsque l’ordinateur de l’utilisateur n’est pas connecté à Internet, les informations contenues dans le document ServiceInfo local sont utilisées pour configurer Lecteur Windows Media pour le service actif initial.

Les paramètres de ligne de commande respectent la casse.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Co-personnalisation des magasins en ligne**](co-branding-online-stores.md)
</dt> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Élément d’installation**](install-element.md)
</dt> <dt>

[**Définition de la boutique en ligne initiale**](setting-the-initial-online-store.md)
</dt> </dl>

 

 




