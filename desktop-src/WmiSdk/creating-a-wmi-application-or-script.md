---
description: Tout langage de script, tel que VBScript, qui fonctionne avec les objets ActiveX peut accéder aux données WMI. Les applications peuvent accéder à WMI en C++, à l’aide de l’API COM pour WMI ou dans Visual Basic, à l’aide de la bibliothèque de types wbemdisp. tlb et de l’API de script pour WMI. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Création d’une application ou d’un script WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27e3cffd7e4d9bea4ce36e7c0da77ae5d72cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521941"
---
# <a name="creating-a-wmi-application-or-script"></a>Création d’une application ou d’un script WMI

Tout langage de script, tel que VBScript, qui fonctionne avec les objets ActiveX peut accéder aux données WMI. Les applications peuvent accéder à WMI en C++, à l’aide [de l’API com pour WMI](com-api-for-wmi.md) ou dans Visual Basic, à l’aide de la [bibliothèque de types](using-the-wmi-scripting-type-library.md) wbemdisp. tlb et de l' [API de script pour WMI](scripting-api-for-wmi.md). . Vous pouvez obtenir des données via WMI en écrivant un script, une page de Active Server (ASP) ou une application HTML (HTA). Vous pouvez également utiliser Windows PowerShell pour obtenir des données ou écrire des scripts. Pour plus d’informations, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) et [prise en main avec Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true). Le ScriptCenter TechNet [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) de contient des centaines d’exemples de script. Pour plus d’informations sur l’impression et les ressources en ligne, consultez plus d' [informations](further-information.md).

La procédure suivante décrit comment se connecter au service WMI et au magasin de données.

**Pour vous connecter au service WMI et à la Banque de données**

1.  Localisez le service WMI sur un ordinateur spécifique.
2.  Connectez-vous à un ou plusieurs espaces de noms WMI.

Ces opérations sont différentes en C++, Visual Basic, .NET Framework langages ou lors de l’utilisation d’un script. Les scripts et les applications Visual Basic doivent accéder aux classes dont les instances sont fournies avec des données par les fournisseurs existants. Mais les applications écrites en C++ peuvent en faire plus. Par exemple, une application écrite en C++ peut envoyer des événements, mais un script WMI peut s’abonner uniquement pour recevoir des événements.

Un fournisseur WMI peut être écrit uniquement en C++ ou à l’aide de l' .NET Framework. Pour plus d’informations sur l’écriture d’applications en C# ou Visual Basic .NET, consultez [vue d’ensemble de WMI .net](/previous-versions/bb404655(v=vs.90)).

Pour plus d’informations sur la création d’applications et de scripts pour WMI, consultez :

-   [Création d’une application WMI à l’aide de C++](creating-a-wmi-application-using-c-.md)
-   [Création d’un script WMI](creating-a-wmi-script.md)
-   [Création d’un client WMI géré](creating-a-managed-wmi-client.md)

Pour effectuer la plupart des tâches, utilisez les [classes WMI](wmi-classes.md)préinstallées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de WMI](using-wmi.md)
</dt> </dl>

 

 
