---
title: ActivationFailureLoggingLevel
description: Définit le niveau de détail des entrées du journal des événements sur les demandes ayant échoué pour le lancement et l’activation des composants.
ms.assetid: c3981621-5826-405c-8962-edfa9c783c2d
keywords:
- Valeur de Registre ActivationFailureLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdd834be35a59dd5d8e207cd679dae68043d70c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363471"
---
# <a name="activationfailurelogginglevel"></a>ActivationFailureLoggingLevel

Définit le niveau de détail des entrées du journal des événements sur les demandes ayant échoué pour le lancement et l’activation des composants.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   ActivationFailureLoggingLevel = value
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **Registre \_ DWORD** .



| Valeur | Description                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Utilisez la journalisation discrétionnaire. Consignez les échecs par défaut, mais les clients peuvent remplacer ce comportement en spécifiant CLSCTX \_ aucun \_ \_ Journal des échecs dans [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex). Il s’agit de la valeur par défaut. |
| 1     | Consigne toujours toutes les défaillances, quel que soit le client spécifié.                                                                                                                                                      |
| 2     | Ne consignez jamais les échecs, quels que soient les éléments spécifiés par le client.                                                                                                                                                       |



 

Si vous avez besoin d’une application pour contrôler la journalisation des événements, il est recommandé de définir cette valeur sur 0 et d’écrire le code client pour la remplacer si nécessaire. Il est vivement recommandé de ne pas définir la valeur sur 2. Si la journalisation des événements est désactivée, il est plus difficile de diagnostiquer les problèmes. Pour les échecs d’autorisation de restrictions d’ordinateur, où COM n’a pas de CLSCTX bits, COM traite une valeur de 0 comme 1.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de la sécurité pour les applications COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




