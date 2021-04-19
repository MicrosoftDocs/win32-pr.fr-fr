---
description: Microsoft XPS document Writer (MXDW) est un pilote d’impression à fichier qui permet à une application Windows de créer des fichiers de document XPS (XML Paper Specification) sur des versions de Windows à partir de Windows XP avec Service Pack 2 (SP2).
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: Microsoft XPS document Writer (MXDW)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c355460112167577c2b6867774c402182084d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520770"
---
# <a name="microsoft-xps-document-writer-mxdw"></a>Microsoft XPS document Writer (MXDW)

Microsoft XPS document Writer (MXDW) est un pilote d’impression à fichier qui permet à une application Windows de créer des fichiers de document XPS (XML Paper Specification) sur des versions de Windows à partir de Windows XP avec Service Pack 2 (SP2). L’utilisation de MXDW permet à une application Windows d’enregistrer son contenu en tant que document XPS sans modifier le code de programme de l’application.

## <a name="when-to-use"></a>Quand l’utiliser

En tant qu’utilisateur, vous devez sélectionner le MXDW lorsque vous souhaitez créer un document XPS à partir d’une application Windows qui n’a pas la possibilité d’enregistrer son contenu en tant que document XPS.

En tant que développeur d’applications, vous recommandez le MXDW aux utilisateurs qui souhaitent créer des documents XPS lorsque votre application n’offre pas la possibilité d’enregistrer en tant que document XPS. Pour plus d’informations sur la spécification XML Paper et les documents XPS, consultez [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) et [XPS Specification et License Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)(en anglais).

Le MXDW est installé automatiquement sur Windows Vista et les versions ultérieures de Windows et peut être téléchargé et installé sur Windows XP avec SP2 et Windows Server 2003.

## <a name="installation"></a>Installation

Sur Windows Vista et les versions ultérieures de Windows, le MXDW est installé automatiquement lors de l’installation du système d’exploitation.

**Windows XP avec SP2 et Windows Server 2003**: téléchargez et installez .net Framework 3,0 ou XPS Essential Pack à partir du [Centre de téléchargement Microsoft](https://www.microsoft.com/downloads/en/default.aspx).

## <a name="how-to-use"></a>Utilisation

Une fois installé, le MXDW apparaît comme une file d’attente à l’impression disponible dans la boîte de dialogue Imprimer présentée par une application. Lorsque le MXDW est sélectionné comme imprimante, l’utilisateur est invité à entrer le nom de fichier à créer comme document XPS qui capture la sortie d’impression de l’application.

L’illustration suivante montre le MXDW sélectionné comme imprimante dans la boîte de dialogue d’impression commune de Windows Vista.

![image de la boîte de dialogue Imprimer qui affiche la sélection de Microsoft XPS document Writer (MXDW)](images/choosingmxdwinvista.gif)

Les développeurs d’applications peuvent personnaliser la sortie de MXDW à l’aide des [paramètres de configuration MXDW](mxdw-configuration-settings.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Spécifications XPS et téléchargements de licences](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Outil de conformité isXPS](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))
</dt> <dt>

[Paramètres de configuration de MXDW](mxdw-configuration-settings.md)
</dt> </dl>

 

 
