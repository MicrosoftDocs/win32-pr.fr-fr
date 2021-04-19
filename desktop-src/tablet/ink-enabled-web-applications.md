---
description: L’exemple de blog Ink illustre plusieurs techniques utiles qui peuvent être utilisées dans des applications Web prenant en charge l’écriture manuscrite.
ms.assetid: 4a5a453d-e3c1-40e6-b0eb-99009f0024dd
title: Applications Web Ink-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b14e368c1d2e97e35afa6d72a0fe082f304c5fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515645"
---
# <a name="ink-enabled-web-applications"></a>Applications Web Ink-Enabled

L’exemple de [blog Ink](ink-blog-web-sample.md) illustre plusieurs techniques utiles qui peuvent être utilisées dans des applications Web prenant en charge l’écriture manuscrite. Il s’agit notamment de vérifier si l’ordinateur client peut prendre en charge des contrôles avec prise en charge de l’encre, envoyer des données d’encre à un serveur et afficher des données manuscrites sur une page Web.

## <a name="testing-ink-enablement"></a>Test de l’activation de l’encre

Il peut être utile de vérifier si l’ordinateur client peut afficher des contrôles à encre activée. Cela vous permet d’avoir un contrôle thewebpageshow si le client est un Tablet PC ou un autre, dans le cas contraire. Une façon de tester cela consiste à tenter de créer un objet tel qu’un objet [InkOverlay](/previous-versions/ms833057(v=msdn.10)), qui peut être créé uniquement sur un ordinateur sur lequel le système d’exploitation Windows Vista, Windows XP Tablet PC Edition ou le kit de développement logiciel (SDK) Windows XP Tablet PC Edition est installé. Si vous créez l’objet à l’intérieur d’un bloc try/catch et interceptez toutes les exceptions levées (souvent, une exception [FileNotFoundException](/previous-versions/windows/) est levée pour indiquer que l’assembly avec ce contrôle est introuvable), vous pouvez détecter si l’ordinateur client peut prendre en charge les contrôles compatibles avec l’encre. Dans l’exemple, ce code se trouve dans le constructeur de la `InkArea` classe.

## <a name="submitting-ink-data"></a>Envoi de données manuscrites

Un moyen simple d’envoyer des données consiste à prendre les données de votre contrôle avec prise en charge de l’encre, à les transférer dans un formulaire masqué, puis à envoyer le formulaire. L’encre peut être sérialisée à l’aide de la méthode [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) , puis convertie en chaîne. Dans l’exemple, le formulaire masqué est défini dans AddBlog. aspx, et la sérialisation de l’encre est gérée dans `InkArea.SerializeInkData` , où l’encre est sérialisée dans une image GIF. (Notez qu’il peut être sérialisé de la même manière dans d’autres formats, par exemple Ink Serialized Format (ISF).)

## <a name="displaying-ink-data"></a>Affichage des données manuscrites

Dans l’exemple, AddBlog. aspx. cs a une méthode appelée `Page_Load` qui récupère les données publiées sur le serveur et les enregistre dans des fichiers. Il génère ensuite des pages Web sur le serveur qui contient des balises IMG qui font référence aux fichiers avec les images GIF. À présent, il vous suffit d’accéder à ces pages pour voir les images de l’encre. (Notez que si vous avez sérialisé l’encre avec un format différent, tel que le format ISF (Ink Serialized Format), vous devez convertir l’encre en image sur le serveur afin de l’afficher sur les clients qui ne sont pas des tablettes.)

Les clients Tablet PC peuvent charger l’encre dans un contrôle avec accès manuscrit et autoriser l’utilisateur à modifier l’encre à l’aide de ISF. Cela est vrai même pour l’encre enregistrée à l’aide de la valeur **gif** de l’énumération [PersistenceFormat](/previous-versions/ms827245(v=msdn.10)) , car les données ISF sont contenues dans les métadonnées gif.

 

 
