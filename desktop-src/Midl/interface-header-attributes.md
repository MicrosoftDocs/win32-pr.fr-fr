---
title: Attributs d’en-tête d’interface
description: Incorporez ces attributs dans l’en-tête d’interface pour transmettre des informations sur l’interface entière.
ms.assetid: 5e30c902-1a55-4afd-afba-93fcc9e75033
keywords:
- IDL MIDL, attributs, en-tête d’interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e5fc25a0e441b092749872a1b4d4735d483cae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029016"
---
# <a name="interface-header-attributes"></a>Attributs d’en-tête d’interface

Incorporez ces attributs dans l’en-tête d’interface pour transmettre des informations sur l’interface entière.



| Attribut                                   | Utilisation                                                                                                                                                                                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_UUID asynchrone**](async-uuid.md)           | Indique au compilateur MIDL de définir à la fois les versions synchrones et asynchrones d’une interface COM.                                                                                                                                               |
| [**universel**](uuid.md)                        | Désigne une valeur 128 bits qui distingue une interface particulière des autres. La valeur réelle peut représenter un GUID, un CLSID ou un IID.                                                                                                 |
| [**localisé**](local.md)                      | Indique au compilateur MIDL de générer uniquement des fichiers d’en-tête. Une interface doit avoir un [**UUID**](uuid.md) ou un attribut [**local**](local.md) .                                                                                             |
| [**MS \_ Union**](-ms-union.md)              | Contrôle l’alignement du rapport de non-remise des unions non encapsulées. Utilisez pour la compatibilité descendante avec les interfaces basées sur MIDL 1,0 ou 2,0.                                                                                                                   |
| [**object**](object.md)                    | Identifie l’interface en tant qu’interface COM et indique au compilateur MIDL de générer le code proxy/stub au lieu des stubs du client et du serveur RPC.                                                                                                    |
| [**Version**](version.md)                  | Identifie une version particulière d’une interface dans les cas où plusieurs versions de l’interface existent. Étant donné que les interfaces COM sont immuables, vous ne pouvez pas utiliser l’attribut [**version**](version.md) sur une interface d' [**objet**](object.md) . |
| [**pointeur \_ par défaut**](pointer-default.md) | Spécifie le type de pointeur par défaut pour tous les pointeurs, à l’exception de ceux inclus dans les listes de paramètres. Le type par défaut peut être [**unique**](unique.md), [**ref**](ref.md)ou [**ptr**](ptr.md).                                                   |
| [**poste**](endpoint.md)                | Spécifie un point de terminaison statique (connu) sur lequel une application serveur doit écouter les appels de procédure distante.                                                                                                                                   |



 

Consultez les [attributs de bibliothèque de types](type-library-attributes.md) pour les attributs d’interface, tels que [**double**](dual.md) et [**oleautomation**](oleautomation.md), qui sont spécifiques aux interfaces définies ou référencées dans une instruction de bibliothèque.

 

 




