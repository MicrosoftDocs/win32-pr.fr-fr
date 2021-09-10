---
title: LocalServer
description: Spécifie le chemin d’accès complet à une application serveur locale 16 bits.
ms.assetid: 6eadadd5-f4d3-4e0d-9491-2ea366861aa7
keywords:
- Clé de Registre LocalServer COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7413f9d7c4d17e9498e80d19b70192fbb21911b6
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363323"
---
# <a name="localserver"></a>LocalServer

Spécifie le chemin d’accès complet à une application serveur locale 16 bits.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer = path
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **reg \_ SZ** qui spécifie le chemin d’accès complet et peut inclure tous les arguments de ligne de commande.

COM ajoute l’indicateur « -Embedding » à la chaîne, de sorte que l’application qui utilise les indicateurs doit analyser l’intégralité de la chaîne et vérifier l’indicateur d’incorporation.

Pour exécuter un serveur d’objets COM dans un espace mémoire séparé, modifiez la valeur de **LocalServer** comme suit :

**cmd/c Start/Separate** *chemin d’accès * * * .exe**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**LocalServer32**](localserver32.md)
</dt> </dl>

 

 




