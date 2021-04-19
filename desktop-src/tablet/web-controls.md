---
description: L’une des façons de créer des applications Web avec accès manuscrit consiste à placer des contrôles de Windows Forms dans awebpagewithin Microsoft Internet Explorer.
ms.assetid: a4fcd692-cd4a-4d2a-bfad-198010e27c6f
title: Contrôles Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b28fa2a3293b6b780412ddbc755634c745b44e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515642"
---
# <a name="web-controls"></a>Contrôles Web

L’une des façons de créer des applications Web avec accès manuscrit consiste à placer des contrôles de Windows Forms dans awebpagewithin Microsoft Internet Explorer. Un bon didacticiel sur cette technique est disponible à [l’aide des contrôles de Windows Forms dans Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx). Les étapes de base du didacticiel sont les suivantes :

1.  Créez un contrôle qui hérite de [**System. Windows. Forms. UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).
2.  Créez une page HTML avec une balise d’objet qui fait référence à ce UserControl.
3.  Créez un répertoire virtuel et définissez des autorisations.
4.  Chargez l’URL de la page HTML dans le navigateur.

Cette technique peut être appliquée à des contrôles compatibles avec l’encre, comme n’importe quel autre [**contrôle**](/dotnet/api/system.windows.forms.control?view=netcore-3.1)de Windows Forms. En fait, la technique peut être utilisée avec n’importe quelle classe de l’infrastructure Microsoft .NET. Les exemples fournis par le kit de développement logiciel (SDK) de Microsoft Windows XP Tablet PC Edition incluent une version de contrôle Web de l’exemple de revendications automatiques dans la section des exemples Web Ink. Cet exemple prend l' [exemple de formulaire de déclaration automatique](auto-claims-form-sample.md) d’origine et le transforme en un contrôle qui est placé sur une page Web. Pour plus d’informations sur l’activation de cet exemple sur le Web, consultez l ['exemple de contrôle Web Ink](ink-web-control-sample.md).

> [!Note]  
> Lorsque vous déployez une application créée à l’aide de .NET sur le Web, l’application peut être affectée par le modèle de sécurité pour .NET. Pour plus d’informations sur le fonctionnement de la sécurité avec les applications Web prenant en charge l’écriture manuscrite, consultez [sécurité et confiance](security-and-trust.md).

 

 

 
