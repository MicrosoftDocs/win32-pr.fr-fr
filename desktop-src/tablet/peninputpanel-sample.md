---
description: Cet exemple s’appuie sur l’exemple de formulaire de revendications automatiques en intégrant l’objet PenInputPanel. L’exemple se trouve dans le \# répertoire C PIPanel du dossier des revendications.
ms.assetid: 9a2c1565-fb24-4767-bfa5-0257129f4bd4
title: Exemple PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c464be52fd08c6c461ba094428a1868fbb51fb328e1a3c88a2d0949a6ae581e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934739"
---
# <a name="peninputpanel-sample"></a>Exemple PenInputPanel

Cet exemple s’appuie sur l’exemple de formulaire de revendications automatiques en intégrant l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) . L’exemple se trouve dans le \# répertoire C PIPanel du dossier des revendications.

> [!Note]  
> Dans cet exemple, votre système doit être équipé d’un appareil Pen. Si vous utilisez juste une souris (ou un autre dispositif de pointage HID), le [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) n’apparaît pas.

 

Pour plus d’informations sur l’exemple de formulaire de déclaration automatique, consultez [exemple de formulaire de déclaration automatique](auto-claims-form-sample.md). Pour plus d’informations sur l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , consultez [programmation du panneau de saisie à l’aide de la classe PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md).

Dans l’exemple, le formulaire de revendications automatiques contient cinq champs dans lesquels l’utilisateur est invité à placer des informations relatives à la revendication : le numéro de la stratégie, le nom assuré, l’année, la marque et le modèle de la voiture. Un objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) est associé à chaque champ d’entrée pour fournir un moyen simple d’entrer des valeurs à l’aide d’un stylet.

Il existe deux techniques pour attacher un objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) aux champs d’entrée de votre formulaire. La première technique consiste à assigner une instance distincte de l’objet à chaque champ d’entrée au moment de la conception. La seconde consiste à créer une instance unique de l’objet, puis à attacher cette instance d’objet au moment de l’exécution à un champ lorsqu’elle reçoit le focus. Cet exemple illustre les deux techniques.

Le choix de la technique à utiliser est lié à des compromis. La création d’une instance unique de l’objet pour chaque champ de formulaire requiert un peu plus de mémoire lorsque le formulaire est chargé. Toutefois, il évite d’avoir à gérer les événements de focus des champs pour assigner une instance unique au champ actuel au moment de l’exécution.

Étant donné que l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) est pris en charge uniquement sur un Tablet PC, l’exemple crée les objets PenInputPanel dans un bloc de gestion des exceptions.

## <a name="one-object-per-field"></a>Un objet par champ

L’exemple illustre la première technique (un objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) par champ) en affectant les champs d’entrée pour le numéro de stratégie ( `inkEdPolicyNumber` ) et le nom assuré ( `inkEdName` ) à une instance unique de l’objet PenInputPanel. Un constructeur surchargé pour l’objet PenInputPanel peut prendre le nom du contrôle d’entrée comme argument, associant ainsi les contrôles. Les lignes suivantes du gestionnaire d’événements [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) du formulaire illustrent ce qui suit :


```C++
pipPolicyNumber = new PenInputPanel(inkEdPolicyNumber);
pipName = new PenInputPanel(inkEdName);
```



## <a name="one-object-per-form"></a>Un objet par formulaire

La deuxième technique est également illustrée dans l’exemple : une seule instance d’un objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , `pipShared` , est partagée entre les champs d’entrée Year, Make et Model. L’objet partagé est créé à l’aide du constructeur par défaut.


```C++
pipShared = new PenInputPanel();
```



L’utilisation de cette technique nécessite que votre formulaire n’ait qu’une seule instance de l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) . Cela permet d’économiser de la mémoire, mais vous devez ajouter du code pour gérer l’événement lorsqu’un champ d’entrée reçoit le focus. Quand un contrôle qui utilise une instance partagée d’un objet PenInputPanel obtient le focus, affectez à la propriété [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) de l’objet PenInputPanel la valeur de ce contrôle. Le code suivant montre un gestionnaire d’événements pour les événements d’année, de marque et de modèle `Enter` .


```C++
private void inkEdYear_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Year field
    pipShared.AttachedEditControl = inkEdYear;

    // set the NUMBER factoid to bias recognition for numbers
    pipShared.Factoid = "NUMBER";

    // Enable correction UI on the inkEdYear field
    pipShared.EnableTsf(true);
}

private void inkEdMake_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Make field
    pipShared.AttachedEditControl = inkEdMake;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdMake field
    pipShared.EnableTsf(true);
}
private void inkEdModel_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Model field
    pipShared.AttachedEditControl = inkEdModel;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdModel field
    pipShared.EnableTsf(true);
}
```



Veillez à définir les propriétés qui doivent être définies lorsque le focus se transforme en nouveau contrôle. Dans les gestionnaires d’événements précédents, par exemple, la propriété [Factoid](/previous-versions/ms571978(v=vs.100)) est définie comme appropriée.

## <a name="usability-considerations"></a>Considérations relatives à la convivialité

Gardez à l’esprit les points suivants à prendre en compte lors de l’utilisation de l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) dans votre application.

### <a name="positioning-the-peninputpanel"></a>Positionnement du PenInputPanel

Étant donné que les champs sont disposés verticalement sur le formulaire de cet exemple, l’interface utilisateur [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) pour chaque contrôle d’entrée est positionnée légèrement à droite du contrôle d’entrée pour en faciliter l’utilisation. Cela empêche le PenInputPanel de couvrir la zone d’édition suivante, ce qui facilite la cible de la zone d’édition suivante.


```C++
pipShared.HorizontalOffset = 32;
pipPolicyNumber.HorizontalOffset = 32;
pipName.HorizontalOffset = 32;
```



### <a name="selecting-input-panel-to-display"></a>Sélection du panneau de saisie à afficher

Étant donné que les numéros de stratégie sont souvent des combinaisons de chiffres, de lettres et d’autres caractères, ils peuvent être sujets à des erreurs de reconnaissance. Par conséquent, l’exemple définit le panneau par défaut affiché par l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) de façon à ce qu’il corresponde au clavier lorsqu’il est associé au champ du numéro de la stratégie.


```C++
pipPolicyNumber.DefaultPanel = PanelType.Keyboard;
```



Le comportement par défaut de l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) est d’utiliser le panneau que l’utilisateur a sélectionné en dernier.

### <a name="text-services-framework-correction-user-interface"></a>Interface utilisateur de correction Text Services Framework

Dans cet exemple, tous les champs d’entrée sont des contrôles [InkEdit](/previous-versions/ms552265(v=vs.100)) . Cela est important, car le contrôle InkEdit intègre une prise en charge de [Text Services Framework](../tsf/text-services-framework.md) (TSF) et peut donc prendre en charge l’interface utilisateur de correction sur place pour les entrées reçues de l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .

La valeur par défaut de [EnableTsf](/previous-versions/ms569656(v=vs.100)) est **true**. L’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) tente alors de démarrer Text Services Framework (TSF) sur le contrôle attaché. En cas de réussite, l’interface utilisateur de correction apparaît dans le contrôle et permet l’accès aux alternatives de reconnaissance. L’appel de cette méthode avec un paramètre **false** tente d’arrêter TSF sur le contrôle attaché.

Le contrôle [InkEdit](/previous-versions/ms552265(v=vs.100)) fournit déjà une interface utilisateur de correction, mais dans l’exemple [EnableTsf](/previous-versions/ms569656(v=vs.100)) est utilisé pour permettre à [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) d’utiliser le contexte du module de reconnaissance d’insertion TSF plutôt que la fonction [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) pour envoyer les résultats de reconnaissance de l’écriture manuscrite dans le contrôle. Le résultat est que du texte peut être inséré même si le champ n’a plus le focus.


```C++
  pipName.EnableTsf(true);
  pipPolicyNumber.EnableTsf(true);
```



## <a name="closing-the-form"></a>Fermeture du formulaire

dans le code généré par le concepteur de formulaires Windows, les contrôles [InkEdit](/previous-versions/ms552265(v=vs.100)) et [InkPicture](/previous-versions/aa514604(v=msdn.10)) sont ajoutés à la liste des composants du formulaire lorsque le formulaire est initialisé. Lorsque le formulaire se ferme, les contrôles InkEdit et InkPicture sont supprimés, ainsi que les autres composants du formulaire, par la méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) du formulaire. La méthode dispose du formulaire supprime également les objets [Ink](/previous-versions/aa515768(v=msdn.10)) créés pour le formulaire.

 

 
