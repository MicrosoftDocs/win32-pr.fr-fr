---
description: Description de l’utilisation de l’objet PenInputPanel pour programmer le panneau de saisie Tablet PC au niveau système.
ms.assetid: f83c7709-86dc-4c64-ad17-2ad660eb57b7
title: Programmation du panneau de saisie à l’aide de la classe PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e00d1cb10983255ab2e532aa08de6e9e6a0fb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320733"
---
# <a name="programming-the-input-panel-using-the-peninputpanel-class"></a>Programmation du panneau de saisie à l’aide de la classe PenInputPanel

\[[**PenInputPanel**](peninputpanel-class.md) a été remplacé par [Microsoft. Ink. TextInput](/previous-versions/ms581554(v=vs.100)). Consultez [programmation du panneau de saisie de texte](programming-the-text-input-panel.md).\]

Description de l’utilisation de l’objet [**PenInputPanel**](peninputpanel-class.md) pour programmer le panneau de saisie Tablet PC au niveau système.

## <a name="input-panel-vs-the-peninputpanel-object"></a>Panneau de saisie et objet PenInputPanel

Dans Microsoft Windows XP Édition Tablet PC version 1,0, le panneau de saisie Tablet PC au niveau du système fournit un mécanisme universel permettant d’effectuer des entrées de texte sur la plate-forme Windows, mais il ne fournit pas d’accès par programme. Dans le kit de développement logiciel (SDK) de Windows XP Édition Tablet PC version 1,5 et versions ultérieures, l’objet [**PenInputPanel**](peninputpanel-class.md) vous permet d’intégrer les outils d’entrée de texte directement dans vos applications et de fournir un niveau de contrôle non disponible précédemment. À compter de Windows XP Édition Tablet PC 2005, le panneau de saisie au niveau du système a été mis à niveau pour inclure les fonctionnalités d’entrée sur place fournies par l’objet **PenInputPanel** et bien plus encore.

Le graphique suivant montre le panneau de saisie affiché sur l’exemple d’exemple de [formulaire de déclaration automatique](auto-claims-form-sample.md) .

![panneau de saisie affiché sur un formulaire utilisé pour les revendications d’automobile](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

Le panneau de saisie remplace le [**PenInputPanel**](peninputpanel-class.md) en fournissant la même fonctionnalité d’entrée sur place à toute application s’exécutant sur Windows XP Édition Tablet PC 2005 ou version ultérieure sans nécessiter de code supplémentaire. Cet article sur l’utilisation de l’objet **PenInputPanel** est fourni à des fins de compatibilité descendante. Les applications qui utilisent déjà l’objet **PenInputPanel** fonctionneront de la même façon, sauf que le panneau de saisie sera affiché à la place du **PenInputPanel** lorsque l’application sera EXÉCUTÉe sur Windows XP Édition Tablet PC 2005 ou version ultérieure.

Si vous développez une nouvelle application pour Tablet PC et que vous souhaitez disposer d’une solution d’entrée d’utilisateur sur place, le panneau de saisie le fournit automatiquement sur Windows XP Édition Tablet PC 2005 ou version ultérieure. Il n’est pas nécessaire d’instancier l’objet [**PenInputPanel**](peninputpanel-class.md) .

## <a name="disabling-the-input-panel"></a>Désactivation du panneau de saisie

Il peut arriver que vous souhaitiez désactiver le panneau de saisie. Il existe deux façons d'accomplir cela. Vous pouvez le faire par programme ou en définissant une entrée de Registre qui désactive le panneau de saisie pour l’ensemble de votre application.

### <a name="disabling-input-panel-programmatically"></a>Désactivation du panneau de saisie par programmation

Pour désactiver le panneau de saisie par programme, instanciez le [**PenInputPanel**](peninputpanel-class.md) et définissez sa propriété [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) sur **false**.


```C++
using Microsoft.Ink;

// ...

private PenInputPanel theInputPanel;

// ...

private void Form1_Load(object sender, System.EventArgs e)
{
// Attach the Input Panel to a specific TextBox control.
theInputPanel = new PenInputPanel(textBox1);

// Disable the Input Panel for the TextBox.
theInputPanel.AutoShow = false;
}
```



Pour désactiver le panneau de saisie pour plusieurs contrôles dans une même application, instanciez un objet [**PenInputPanel**](peninputpanel-class.md) pour chaque contrôle et affectez la valeur **false** à la propriété [**affichage**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)automatique pour chaque ou instanciez un **PenInputPanel** unique et déplacez-le du contrôle au contrôle en tant que Focus d’entrée. Pour plus d’informations sur ces deux techniques, consultez l’exemple de rubrique [PenInputPanel](peninputpanel-sample.md) .

### <a name="disabling-input-panel-through-the-registry"></a>Désactivation du panneau de saisie dans le registre

Vous pouvez définir une entrée de Registre pour désactiver le panneau de saisie pour l’ensemble de votre application. Toutefois, cette opération est également désactivée pour les boîtes de dialogue courantes telles que la boîte de dialogue **ouvrir un fichier** , la boîte de dialogue **Imprimer** et la boîte de dialogue **enregistrement de fichier** . Cela peut rendre l’expérience utilisateur dans votre application incohérente avec les autres applications Tablet PC.

La définition de la `DisableInPlace` clé de Registre sur zéro empêche l’affichage de l’interface utilisateur du panneau de saisie dans une application. Vous devez placer la `DisableInPlace` clé de Registre à l’emplacement `HKEY_LOCAL_MACHINE\Software\Microsoft\TabletTip\` . Ensuite, ajoutez une nouvelle valeur de registre en utilisant le chemin d’accès complet de l’application dans laquelle vous souhaitez désactiver le panneau de saisie. L’exemple d’entrée de Registre suivant désactive le panneau de saisie dans une application nommée MyApp :

`[HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\WindowsNT\TabletTIP\DisableInPlace]``"C:\Program Files\My App\MyApp.exe"=dword:00000000`

Si vous rencontrez toujours un problème dans votre application après avoir désactivé l’interface utilisateur du panneau de saisie, il peut être nécessaire de désactiver l’infrastructure sous-jacente, qui interroge votre application à la recherche de l’emplacement du signe insertion. Par exemple, le panneau de saisie peut exposer un bogue dans le code de suivi du signe insertion de votre application. La désactivation de la requête de suivi du signe insertion empêche également l’interface utilisateur du panneau de saisie d’apparaître. Pour désactiver le Framework, définissez la `EnableCaretTracking` clé de Registre sur zéro. Localisez cette clé à l’adresse `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\AppCompatFlags\CaretTracking\` .

> [!Note]  
> Les outils d’accessibilité et la technologie vocale de Windows XP utilisent également ce Framework. par conséquent, la désactivation de la requête désactive également ces fonctionnalités dans votre application.

 

## <a name="the-input-panel-and-web-pages"></a>Le panneau de saisie et les pages Web

Pour pouvoir utiliser une API sur une page Web, elle doit fonctionner dans un environnement de confiance partielle. Tous les membres de la classe [**PenInputPanel**](peninputpanel-class.md) requièrent une confiance totale, à l’exception des éléments suivants :

-   [Constructeurs PenInputPanel](/previous-versions/dotnet/netframework-3.5/ms571341(v=vs.90)) (code managé uniquement)
-   [Dispose, méthode](/previous-versions/dotnet/netframework-3.5/ms571343(v=vs.90)) (code managé uniquement)
-   [Propriété AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (code managé uniquement)
-   [**Affichage automatique, propriété**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)

Ces API fonctionnent dans un environnement de confiance partielle, tel qu’une page Web, vous permettant d’instancier un objet [**PenInputPanel**](peninputpanel-class.md) , de l’attacher à un contrôle et de désactiver le panneau de saisie pour ce contrôle. Pour plus d’informations, consultez programmation du panneau de saisie à l’aide de la classe PenInputPanel et [de l’encre sur le Web](ink-on-the-web.md).

## <a name="the-peninputpanel-object"></a>Objet PenInputPanel

Le reste de cette rubrique explique comment utiliser l’objet [**PenInputPanel**](peninputpanel-class.md) dans vos applications compatibles avec Tablet PC. Plus spécifiquement, cette rubrique fait référence à l’objet **PenInputPanel** lorsqu’il s’agit de décrire l’objet de programmation, le panneau de saisie du stylet pour faire référence à l’élément d’interface utilisateur et le panneau de saisie du PC (ou le panneau de saisie) quand vous faites référence au panneau de saisie global généralement situé sur le côté de l’écran du Tablet PC.

Les sections suivantes décrivent l’objet [**PenInputPanel**](peninputpanel-class.md) et l’interface utilisateur.

-   [À propos du panneau de saisie](about-the-input-panel.md)
-   [Instanciation de la classe PenInputPanel](instantiating-the-peninputpanel-class.md)
-   [Support Factoid](factoid-support.md)
-   [Text Services Framework](text-services-framework.md)
-   [Bonnes pratiques](best-practices.md)

 

 
