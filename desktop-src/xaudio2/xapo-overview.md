---
description: l’API XAPO permet la création d’objets de traitement audio multiplateforme (XAPO) pour une utilisation dans XAudio2 à la fois sur Windows et sur Xbox 360.
ms.assetid: 4fe88a0f-0234-462f-b575-e592f2c8401e
title: Présentation de XAPO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e2372790e26b7fcd3d15019797185ba180d668
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521969"
---
# <a name="xapo-overview"></a>Présentation de XAPO

l’API XAPO permet la création d’objets de traitement audio multiplateforme (XAPO) pour une utilisation dans XAudio2 à la fois sur Windows et sur Xbox 360. Un XAPO est un objet qui utilise des données audio entrantes et effectue une opération sur les données avant de les transmettre. Vous pouvez utiliser un XAPO pour effectuer diverses tâches, notamment ajouter un verbe à un flux audio et surveiller les niveaux de volume des pics.

## <a name="creating-new-xapos"></a>Création de XAPOs

L’API XAPO fournit l’interface [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) et la classe [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) pour la génération de nouveaux types XAPO. L’interface **IXAPO** contient toutes les méthodes qui doivent être implémentées pour créer un nouveau XAPO. La classe **CXAPOBase** fournit une implémentation de base de l’interface **IXAPO** . **CXAPOBase** implémente toutes les méthodes d’interface **IXAPO** , à l’exception de la méthode [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , qui est unique à chaque XAPO.

Pour obtenir un exemple de création d’un nouveau XAPO, consultez [Comment : créer un XAPO](how-to--create-an-xapo.md).

Pour obtenir un exemple de création d’un XAPO qui accepte des paramètres au moment de l’exécution, consultez [Comment : ajouter la prise en charge des paramètres d’exécution à un XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).

## <a name="xapos-and-com"></a>XAPOs et COM

XAPOs implémente l’interface **IUnknown** . Les interfaces [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) et [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) incluent les trois méthodes **IUnknown** : **QueryInterface**, **AddRef** et **Release**. [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) fournit des implémentations des trois méthodes IUnknown. Une nouvelle instance de **CXAPOBase** aura un compte de référence de 1. Elle sera détruite quand son décompte de références devient 0. Les implémentations de **IXAPO** et **IXAPOParameters** doivent suivre le même modèle pour permettre la gestion appropriée lorsqu’elles sont utilisées avec XAudio2.

Les instances XAPO sont passées à XAudio2 en tant qu’interfaces **IUnknown** . XAudio2 utilise **QueryInterface** pour acquérir une interface [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) et détecter si le XAPO implémente l’interface [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) . Les implémentations de **IXAPO** doivent accepter les demandes pour **\_ \_ uuidof (IXAPO)**. Si **IXAPOParameters** est implémenté, il doit également accepter les demandes pour **\_ \_ uuidof (IXAPOParameters)**.

## <a name="using-an-xapo-in-xaudio2"></a>Utilisation d’un XAPO dans XAudio2

Les XAPOs sont utilisés dans XAudio2 en les joignant à des voix. Chaque voix XAudio2 a une chaîne d’effet contenant zéro ou plusieurs effets audio. Les données audio envoyées à une voix sont transmises à chaque effet de la chaîne avant d’être envoyées aux cibles de sortie de la voix. Les données sont transmises de la voix à chaque effet à l’aide du paramètre *pInputProcessParameters* de la méthode [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process) . Ensuite, il est renvoyé à la voix à l’aide du paramètre *pOutputProcessParameters* . La voix prend la sortie de chaque effet et l’alimente dans l’effet suivant de la chaîne jusqu’à ce qu’aucun effet ne reste dans la chaîne.

Pour plus d’informations sur les chaînes d’effets XAudio2, consultez [effets audio XAudio2](xaudio2-audio-effects.md).

Pour obtenir un exemple d’utilisation d’un XAPO dans XAudio2, consultez [Comment : utiliser un XAPO dans XAudio2](how-to--use-an-xapo-in-xaudio2.md).

## <a name="effect-libraries"></a>Bibliothèques d’effets

La bibliothèque d’effets XAPO contient plusieurs XAPOs, et une méthode courante pour les instancier. Pour plus d’informations sur XAPOFX, consultez [vue d’ensemble de XAPOFX](xapofx-overview.md) . En outre, XAudio2 a des effets de réverbération et de mesure de volume intégrés. Pour plus d’informations sur les effets XAudio2 intégrés, consultez [effets audio XAudio2](xaudio2-audio-effects.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets audio](audio-effects.md)
</dt> <dt>

[Effets audio XAudio2](xaudio2-audio-effects.md)
</dt> </dl>

 

 
