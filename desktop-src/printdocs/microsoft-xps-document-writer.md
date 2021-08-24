---
description: Microsoft XPS Document Writer (MXDW) est un pilote d’impression à fichier qui permet à un Windows application de créer des fichiers de Document XPS (XML Paper Specification) sur des versions de Windows à partir de Windows XP avec Service Pack 2 (SP2).
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: Microsoft XPS document Writer (MXDW)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dba69a6efff4f2da0ab0cc03bdc71468dada14c457de7685053096d2fba672d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938883"
---
# <a name="microsoft-xps-document-writer-mxdw"></a>Microsoft XPS document Writer (MXDW)

Microsoft XPS Document Writer (MXDW) est un pilote d’impression à fichier qui permet à un Windows application de créer des fichiers de Document XPS (XML Paper Specification) sur des versions de Windows à partir de Windows XP avec Service Pack 2 (SP2). l’utilisation de MXDW permet à une application Windows d’enregistrer son contenu sous la forme d’un document XPS sans modifier le code du programme de l’application.

## <a name="when-to-use"></a>Quand l’utiliser

en tant qu’utilisateur, vous devez sélectionner le MXDW lorsque vous souhaitez créer un document xps à partir d’une application Windows qui n’a pas la possibilité d’enregistrer son contenu en tant que document xps.

En tant que développeur d’applications, vous recommandez le MXDW aux utilisateurs qui souhaitent créer des documents XPS lorsque votre application n’offre pas la possibilité d’enregistrer en tant que document XPS. Pour plus d’informations sur la spécification XML Paper et les documents XPS, consultez [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) et [XPS Specification et License Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)(en anglais).

le MXDW est installé automatiquement sur Windows Vista et les versions ultérieures de Windows et peut être téléchargé et installé sur Windows XP avec SP2 et Windows Server 2003.

## <a name="installation"></a>Installation

sur Windows Vista et les versions ultérieures de Windows, MXDW est installé automatiquement lors de l’installation du système d’exploitation.

**Windows XP avec SP2 et Windows Server 2003**: téléchargez et installez .net Framework 3,0 ou XPS Essential Pack à partir du [centre de téléchargement Microsoft](https://www.microsoft.com/downloads/en/default.aspx).

## <a name="how-to-use"></a>Utilisation

Une fois installé, le MXDW apparaît comme une file d’attente à l’impression disponible dans la boîte de dialogue Imprimer présentée par une application. Lorsque le MXDW est sélectionné comme imprimante, l’utilisateur est invité à entrer le nom de fichier à créer comme document XPS qui capture la sortie d’impression de l’application.

l’illustration suivante montre le MXDW sélectionné comme imprimante dans la boîte de dialogue d’impression commune Windows Vista.

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

 

 
