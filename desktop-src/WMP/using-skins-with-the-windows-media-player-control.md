---
title: Utilisation d’habillages avec le contrôle du lecteur Windows Media
description: Utilisation d’habillages avec le contrôle du lecteur Windows Media
ms.assetid: 0381e0e4-c686-4ab4-b947-b883b6f4e06e
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Lecteur Windows Media, C++
- Windows Media Player Object Model, C++
- modèle objet, C++
- Windows Media Player Mobile, C++
- Contrôle ActiveX du lecteur Windows Media, C++
- Windows Media Player Mobile, contrôle ActiveX, C++
- Contrôle ActiveX, C++
- Incorporation de programmes C++
- incorporation, programmes C++
- Contrôle ActiveX du lecteur Windows Media, apparences
- Windows Media Player Mobile contrôle ActiveX, Skins
- Contrôle ActiveX, apparences
- apparences, incorporer un contrôle ActiveX
- Apparences du lecteur Windows Media, incorporer un contrôle ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714a8be9e471541d008fcb76a4b0398dba2162b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196811"
---
# <a name="using-skins-with-the-windows-media-player-control"></a>Utilisation d’habillages avec le contrôle du lecteur Windows Media

Lorsque vous incorporez le contrôle du lecteur Windows Media dans un programme C++, vous pouvez personnaliser l’interface utilisateur du lecteur en lui appliquant un fichier de définition d’apparence. Un fichier de définition d’apparence est un document XML qui spécifie la disposition des composants d’interface utilisateur standard et personnalisables, ainsi que les graphiques qui l’accompagnent. À l’aide de Microsoft JScript, vous pouvez spécifier le comportement de ces composants et manipuler le contrôle du lecteur Windows Media sans la surcharge de la syntaxe C++ et COM.

Les apparences permettent de conserver facilement votre code d’interface utilisateur et votre code de programme principal afin qu’ils puissent être gérés et développés indépendamment. Vous pouvez également réutiliser des apparences conçues à l’origine pour une utilisation par le lecteur autonome en mode apparence. Le code d’apparence que vous concevez spécifiquement pour les programmes C++ peut interagir avec vos programmes par le biais d’un objet scriptable que votre programme peut fournir.

Pour activer le mode apparence pour le contrôle du lecteur Windows Media, votre programme doit implémenter l’interface **IWMPRemoteMediaServices** . Bien que vous puissiez utiliser les apparences avec le contrôle et le contrôle à distance en même temps, vous pouvez utiliser cette interface pour activer l’une ou l’autre des fonctionnalités sans activer l’autre. Pour désactiver la communication à distance, transmettez simplement une valeur « local » comme paramètre de sortie de la méthode **GetServiceType** et retournez un HRESULT de E \_ NOTIMPL à partir de la méthode **GetApplicationName** .

Pour basculer le contrôle du lecteur Windows Media en mode apparence, appelez la méthode **IWMPPlayer ::p ut \_ UIMODE** , en passant la valeur « Custom ». Spécifiez le chemin d’accès et le nom de fichier du fichier de définition d’apparence à utiliser en le renvoyant à partir de la méthode **IWMPRemoteMediaServices :: GetCustomUIMode** .

Si vous souhaitez fournir un objet scriptable pour la communication entre votre apparence et votre programme, transmettez un nom et un pointeur vers un pointeur **IDispatch** en tant que deux paramètres de sortie de la méthode **IWMPRemoteMediaServices :: GetScriptableObject** . Votre apparence peut ensuite effectuer des appels à l’objet scriptable en utilisant le nom spécifié comme s’il s’agissait d’un attribut global similaire à l’attribut global **Player** .

Une apparence appliquée à un contrôle du lecteur Windows Media distant peut accéder à l’objet **PlayerApplication** à l’aide d’un autre attribut global appelé **PlayerApplication**. Étant donné que la propriété **Player. playerApplication** n’est pas accessible par les apparences, vous devez utiliser cet attribut global lorsque vous souhaitez que votre code de peau gère l’ancrage et la déconnexion.

## <a name="samples"></a>Exemples

Le package d’installation du kit de développement logiciel (SDK) Windows Media Player installe un exemple qui illustre l’application d’une apparence au contrôle du lecteur Windows Media. Pour plus d’informations, consultez l’exemple RemoteSkin.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemples**](samples.md)
</dt> <dt>

[**Utilisation du contrôle du lecteur Windows Media dans un programme C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




