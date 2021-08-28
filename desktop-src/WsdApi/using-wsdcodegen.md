---
description: Décrit le processus de création d’une application WSDAPI à l’aide de WsdCodeGen.
ms.assetid: 8f172e2c-4cd1-4108-9c8d-01a731aca83b
title: Utilisation de WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6395d39a84415cc56e66949ea82ef7a1acd9fc009b7e1b2c93fa2712e8a81a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463169"
---
# <a name="using-wsdcodegen"></a>Utilisation de WsdCodeGen

**Pour générer une application WSDAPI à l’aide de WsdCodeGen**

1.  Définissez le contrat fonctionnel pour l’hôte d’appareil dans un fichier WSDL.
2.  Générez un fichier de configuration à l’aide de WsdCodeGen. Pour plus d’informations, consultez [fichier de configuration WsdCodeGen](wsdcodegen-configuration-file.md) et syntaxe de la [ligne de commande WsdCodeGen](wsdcodegen-command-line-syntax.md).
3.  Ouvrez le fichier de configuration généré, puis modifiez le fichier en fonction de vos besoins. Si vous générez une application cliente, peu ou aucune modification n’est requise. Si vous générez une application hôte, modifiez les éléments de configuration spécifiques à l’utilisateur (tels que [**fabricant**](manufacturer.md) et [**modelname**](modelname.md)).
4.  Générez le code à l’aide de WsdCodeGen, en fournissant le fichier de configuration en tant qu’entrée. Pour plus d’informations, consultez Syntaxe de la [ligne de commande WsdCodeGen](wsdcodegen-command-line-syntax.md).
5.  Utilisez le code généré pour générer un client, un hôte, ou les deux.

le SDK Windows comprend des exemples de fichiers WSDL, des fichiers de configuration WsdCodeGen et du code généré. Pour plus d’informations, consultez [exemples wsdapi](wsdapi-samples.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples WSDAPI](wsdapi-samples.md)
</dt> </dl>

 

 



