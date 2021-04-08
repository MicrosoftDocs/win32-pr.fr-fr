---
title: Écriture de scripts avec des objets COM
description: Écriture de scripts avec des objets COM
ms.assetid: d99a561b-67dc-4fc9-adfa-cd7350eb16ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2b00380a14db2d254675a5826b61f262e8cfe8
ms.sourcegitcommit: 8c981a2f4149b4a9d605ffb71fefda8d82bc696e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2019
ms.locfileid: "103677977"
---
# <a name="scripting-with-com-objects"></a>Écriture de scripts avec des objets COM

Un *langage de script* est un langage de programmation qui est analysé au moment de l’exécution par un *moteur de script*, un composant qui traduit les scripts écrits dans ce langage dans le code machine. Chaque moteur de script traduit un langage de script spécifique. Un *hôte de script* est une application, telle qu’un navigateur Web, qui héberge un moteur de script pour exécuter des scripts. Si votre hôte de script prend en charge COM, vous pouvez écrire des scripts qui utilisent des objets COM. Les rubriques suivantes décrivent les hôtes de script qui prennent en charge les objets COM, les langages de script courants et les méthodes de conversion entre les langages de script.

Un langage de script diffère d’un langage compilé dans le fait qu’il est traduit en code machine au moment de l’exécution. Cela signifie que chaque fois que vous exécutez un script, le moteur de script analyse d’abord le code, puis l’exécute. En revanche, les langages compilés, tels que C++, sont traduits une seule fois en code machine, pendant la compilation. Lorsque vous exécutez une application compilée, le système d’exploitation exécute simplement le code précompilé.

Étant donné qu’un moteur de script doit analyser un script chaque fois qu’il s’exécute, les langages de script sont généralement plus lents et moins efficaces que leurs équivalents précompilés. Toutefois, l’avantage des scripts est qu’ils sont faciles à écrire et à gérer. Les langages de script sont généralement plus simples que les langages précompilés, et lorsqu’un script change, il n’a pas besoin d’être recompilé. Pour les applications légères et à variation rapide, telles que les pages Web, les langages de script sont idéaux.

Il existe plusieurs environnements hôtes dans lesquels vous pouvez écrire des scripts qui utilisent des objets COM, comme décrit ci-après :

-   [Incorporation d’objets COM dans des pages Web](embedding-com-objects-in-web-pages.md)
-   [Utilisation d’objets COM dans des pages Active Server](using-com-objects-in-active-server-pages.md)
-   [Utilisation d’objets COM dans Windows Script Host](using-com-objects-in-windows-script-host.md)
-   [Écriture de scripts d’objets COM dans des applications personnalisées](scripting-com-objects-in-custom-applications.md)

Dans chacun des environnements d’hôte mentionnés précédemment, un moteur de script analyse et exécute le script. Étant donné que le moteur de chaque langage de script est un composant distinct, vous pouvez ajouter un nouveau langage de script à un environnement en ajoutant un nouveau moteur.

Les langages de script les plus couramment utilisés sont les suivants :

-   Microsoft Visual Basic Scripting Edition (VBScript), un sous-ensemble de Visual Basic.
-   JavaScript, le langage de script de Netscape, anciennement appelé LiveScript.
-   Logiciel de développement Microsoft JScript, implémentation Microsoft de la spécification du langage ECMA 262.

Microsoft fournit des moteurs de script pour JScript et VBScript. D’autres éditeurs de logiciels fournissent des moteurs de script ActiveX pour les langages tels que PerlScript, PScript, Python, etc.

Pour plus d’informations, consultez la [spécification du langage ECMA 262](https://www.ecma-international.org/publications/standards/Ecma-262.htm).

Notez que la plupart des langages de script, tels que VBScript et JScript, ne peuvent pas accéder ou modifier des fichiers. Cette incapacité empêche le script de modifier les données sur les ordinateurs clients. Toutefois, les objets COM n’ont pas de telles limitations. Une fois qu’elles sont téléchargées et installées sur les ordinateurs clients, elles peuvent effectuer n’importe quelle action d’application standard. Par conséquent, les utilisateurs doivent uniquement télécharger et exécuter des contrôles ActiveX provenant de sources approuvées.

Pour plus d’informations sur la traduction entre les langages de script, consultez les rubriques suivantes :

-   [Conversion en VBScript](translating-to-vbscript.md)
-   [Traduire en JScript](translating-to-jscript.md)
-   [Conversion en JavaScript](translating-to-javascript.md)

 

 




