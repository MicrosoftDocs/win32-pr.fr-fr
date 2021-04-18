---
description: Cet exemple s’appuie sur l’exemple de formulaire de revendications automatiques en intégrant l’objet PenInputPanel. L’exemple se trouve dans le \# répertoire C PIPanel du dossier des revendications.
ms.assetid: 9a2c1565-fb24-4767-bfa5-0257129f4bd4
title: Exemple PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d60f33ff3f61e1a2930841e5fd3d3ce3f9fc5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526272"
---
# <a name="peninputpanel-sample"></a><span data-ttu-id="e313b-104">Exemple PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="e313b-104">PenInputPanel Sample</span></span>

<span data-ttu-id="e313b-105">Cet exemple s’appuie sur l’exemple de formulaire de revendications automatiques en intégrant l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="e313b-105">This sample builds on the Auto Claims Form sample by integrating the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span> <span data-ttu-id="e313b-106">L’exemple se trouve dans le \# répertoire C PIPanel du dossier des revendications.</span><span class="sxs-lookup"><span data-stu-id="e313b-106">The sample is in the C\# PIPanel directory in the AutoClaims folder.</span></span>

> [!Note]  
> <span data-ttu-id="e313b-107">Dans cet exemple, votre système doit être équipé d’un appareil Pen.</span><span class="sxs-lookup"><span data-stu-id="e313b-107">This sample requires that your system is equipped with a pen device.</span></span> <span data-ttu-id="e313b-108">Si vous utilisez juste une souris (ou un autre dispositif de pointage HID), le [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) n’apparaît pas.</span><span class="sxs-lookup"><span data-stu-id="e313b-108">If you are using just a mouse (or other non-human interface device (HID) pointing device) the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) does not appear.</span></span>

 

<span data-ttu-id="e313b-109">Pour plus d’informations sur l’exemple de formulaire de déclaration automatique, consultez [exemple de formulaire de déclaration automatique](auto-claims-form-sample.md).</span><span class="sxs-lookup"><span data-stu-id="e313b-109">For more information about the Auto Claims Form sample, see [Auto Claims Form Sample](auto-claims-form-sample.md).</span></span> <span data-ttu-id="e313b-110">Pour plus d’informations sur l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , consultez [programmation du panneau de saisie à l’aide de la classe PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md).</span><span class="sxs-lookup"><span data-stu-id="e313b-110">For more information about the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object, see [Programming the Input Panel Using the PenInputPanel Class](programming-the-input-panel-using-the-peninputpanel-class.md).</span></span>

<span data-ttu-id="e313b-111">Dans l’exemple, le formulaire de revendications automatiques contient cinq champs dans lesquels l’utilisateur est invité à placer des informations relatives à la revendication : le numéro de la stratégie, le nom assuré, l’année, la marque et le modèle de la voiture.</span><span class="sxs-lookup"><span data-stu-id="e313b-111">In the sample, the Auto Claims Form contains five fields into which the user is asked to put information relevant to the claim: policy number, insured name, the year, make, and model of the car.</span></span> <span data-ttu-id="e313b-112">Un objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) est associé à chaque champ d’entrée pour fournir un moyen simple d’entrer des valeurs à l’aide d’un stylet.</span><span class="sxs-lookup"><span data-stu-id="e313b-112">A [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is attached to each input field to provide an easy means for entering values with a pen.</span></span>

<span data-ttu-id="e313b-113">Il existe deux techniques pour attacher un objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) aux champs d’entrée de votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="e313b-113">There are two techniques for attaching a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to the input fields on your form.</span></span> <span data-ttu-id="e313b-114">La première technique consiste à assigner une instance distincte de l’objet à chaque champ d’entrée au moment de la conception.</span><span class="sxs-lookup"><span data-stu-id="e313b-114">The first technique is to assign a separate instance of the object to each input field at design time.</span></span> <span data-ttu-id="e313b-115">La seconde consiste à créer une instance unique de l’objet, puis à attacher cette instance d’objet au moment de l’exécution à un champ lorsqu’elle reçoit le focus.</span><span class="sxs-lookup"><span data-stu-id="e313b-115">The second is to create a single instance of the object and then attach that object instance at run time to a field when it receives focus.</span></span> <span data-ttu-id="e313b-116">Cet exemple illustre les deux techniques.</span><span class="sxs-lookup"><span data-stu-id="e313b-116">This sample demonstrates both techniques.</span></span>

<span data-ttu-id="e313b-117">Le choix de la technique à utiliser est lié à des compromis.</span><span class="sxs-lookup"><span data-stu-id="e313b-117">There are tradeoffs involved in deciding which technique to use.</span></span> <span data-ttu-id="e313b-118">La création d’une instance unique de l’objet pour chaque champ de formulaire requiert un peu plus de mémoire lorsque le formulaire est chargé.</span><span class="sxs-lookup"><span data-stu-id="e313b-118">Creating a unique instance of the object for each form field requires slightly more memory when the form is loaded.</span></span> <span data-ttu-id="e313b-119">Toutefois, il évite d’avoir à gérer les événements de focus des champs pour assigner une instance unique au champ actuel au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="e313b-119">However, it saves having to handle focus events for the fields to assign a single instance to the current field at run time.</span></span>

<span data-ttu-id="e313b-120">Étant donné que l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) est pris en charge uniquement sur un Tablet PC, l’exemple crée les objets PenInputPanel dans un bloc de gestion des exceptions.</span><span class="sxs-lookup"><span data-stu-id="e313b-120">Because the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is supported only on a Tablet PC, the sample creates the PenInputPanel objects within an exception-handling block.</span></span>

## <a name="one-object-per-field"></a><span data-ttu-id="e313b-121">Un objet par champ</span><span class="sxs-lookup"><span data-stu-id="e313b-121">One Object per Field</span></span>

<span data-ttu-id="e313b-122">L’exemple illustre la première technique (un objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) par champ) en affectant les champs d’entrée pour le numéro de stratégie ( `inkEdPolicyNumber` ) et le nom assuré ( `inkEdName` ) à une instance unique de l’objet PenInputPanel.</span><span class="sxs-lookup"><span data-stu-id="e313b-122">The sample demonstrates the first technique (one [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object per field) by assigning the input fields for policy number (`inkEdPolicyNumber`) and insured name (`inkEdName`) a unique instance of the PenInputPanel object.</span></span> <span data-ttu-id="e313b-123">Un constructeur surchargé pour l’objet PenInputPanel peut prendre le nom du contrôle d’entrée comme argument, associant ainsi les contrôles.</span><span class="sxs-lookup"><span data-stu-id="e313b-123">An overloaded constructor for the PenInputPanel object can take the name of the input control as an argument, thus associating the controls.</span></span> <span data-ttu-id="e313b-124">Les lignes suivantes du gestionnaire d’événements [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) du formulaire illustrent ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="e313b-124">The following lines from the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler shows this:</span></span>


```C++
pipPolicyNumber = new PenInputPanel(inkEdPolicyNumber);
pipName = new PenInputPanel(inkEdName);
```



## <a name="one-object-per-form"></a><span data-ttu-id="e313b-125">Un objet par formulaire</span><span class="sxs-lookup"><span data-stu-id="e313b-125">One Object per Form</span></span>

<span data-ttu-id="e313b-126">La deuxième technique est également illustrée dans l’exemple : une seule instance d’un objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , `pipShared` , est partagée entre les champs d’entrée Year, Make et Model.</span><span class="sxs-lookup"><span data-stu-id="e313b-126">The second technique is also shown in the sample: a single instance of a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object, `pipShared`, is shared between the Year, Make, and Model input fields.</span></span> <span data-ttu-id="e313b-127">L’objet partagé est créé à l’aide du constructeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e313b-127">The shared object is created by using the default constructor.</span></span>


```C++
pipShared = new PenInputPanel();
```



<span data-ttu-id="e313b-128">L’utilisation de cette technique nécessite que votre formulaire n’ait qu’une seule instance de l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="e313b-128">Using this technique requires that your form have only a single instance of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span> <span data-ttu-id="e313b-129">Cela permet d’économiser de la mémoire, mais vous devez ajouter du code pour gérer l’événement lorsqu’un champ d’entrée reçoit le focus.</span><span class="sxs-lookup"><span data-stu-id="e313b-129">This saves memory, but you must add code to handle the event when an input field receives focus.</span></span> <span data-ttu-id="e313b-130">Quand un contrôle qui utilise une instance partagée d’un objet PenInputPanel obtient le focus, affectez à la propriété [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) de l’objet PenInputPanel la valeur de ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="e313b-130">When a control that uses a shared instance of a PenInputPanel object gets focus, set the PenInputPanel object's [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) property to that control.</span></span> <span data-ttu-id="e313b-131">Le code suivant montre un gestionnaire d’événements pour les événements d’année, de marque et de modèle `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e313b-131">The following code shows an event handler for the Year, Make, and Model fields' `Enter` events.</span></span>


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



<span data-ttu-id="e313b-132">Veillez à définir les propriétés qui doivent être définies lorsque le focus se transforme en nouveau contrôle.</span><span class="sxs-lookup"><span data-stu-id="e313b-132">Be sure to set any properties that need to be set when focus changes to a new control.</span></span> <span data-ttu-id="e313b-133">Dans les gestionnaires d’événements précédents, par exemple, la propriété [Factoid](/previous-versions/ms571978(v=vs.100)) est définie comme appropriée.</span><span class="sxs-lookup"><span data-stu-id="e313b-133">In the previous event handlers, for example, the [Factoid](/previous-versions/ms571978(v=vs.100)) property is set as appropriate.</span></span>

## <a name="usability-considerations"></a><span data-ttu-id="e313b-134">Considérations relatives à la convivialité</span><span class="sxs-lookup"><span data-stu-id="e313b-134">Usability Considerations</span></span>

<span data-ttu-id="e313b-135">Gardez à l’esprit les points suivants à prendre en compte lors de l’utilisation de l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) dans votre application.</span><span class="sxs-lookup"><span data-stu-id="e313b-135">Keep the following usability considerations in mind when using the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object in your application.</span></span>

### <a name="positioning-the-peninputpanel"></a><span data-ttu-id="e313b-136">Positionnement du PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="e313b-136">Positioning the PenInputPanel</span></span>

<span data-ttu-id="e313b-137">Étant donné que les champs sont disposés verticalement sur le formulaire de cet exemple, l’interface utilisateur [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) pour chaque contrôle d’entrée est positionnée légèrement à droite du contrôle d’entrée pour en faciliter l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="e313b-137">Because the fields are laid out vertically on the form in this sample, the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) user interface for each input control is positioned slightly to the right of the input control to make it easier to use.</span></span> <span data-ttu-id="e313b-138">Cela empêche le PenInputPanel de couvrir la zone d’édition suivante, ce qui facilite la cible de la zone d’édition suivante.</span><span class="sxs-lookup"><span data-stu-id="e313b-138">This prevents the PenInputPanel from covering up the next edit box, making it easier to target the next edit box.</span></span>


```C++
pipShared.HorizontalOffset = 32;
pipPolicyNumber.HorizontalOffset = 32;
pipName.HorizontalOffset = 32;
```



### <a name="selecting-input-panel-to-display"></a><span data-ttu-id="e313b-139">Sélection du panneau de saisie à afficher</span><span class="sxs-lookup"><span data-stu-id="e313b-139">Selecting Input Panel to Display</span></span>

<span data-ttu-id="e313b-140">Étant donné que les numéros de stratégie sont souvent des combinaisons de chiffres, de lettres et d’autres caractères, ils peuvent être sujets à des erreurs de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="e313b-140">Because policy numbers are often combinations of numbers, letters, and other characters, they can be prone to recognition errors.</span></span> <span data-ttu-id="e313b-141">Par conséquent, l’exemple définit le panneau par défaut affiché par l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) de façon à ce qu’il corresponde au clavier lorsqu’il est associé au champ du numéro de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="e313b-141">Therefore, the sample sets the default panel displayed by the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to be the keyboard when it is attached to the policy number field.</span></span>


```C++
pipPolicyNumber.DefaultPanel = PanelType.Keyboard;
```



<span data-ttu-id="e313b-142">Le comportement par défaut de l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) est d’utiliser le panneau que l’utilisateur a sélectionné en dernier.</span><span class="sxs-lookup"><span data-stu-id="e313b-142">The default behavior of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object is to use the panel the user selected last.</span></span>

### <a name="text-services-framework-correction-user-interface"></a><span data-ttu-id="e313b-143">Interface utilisateur de correction Text Services Framework</span><span class="sxs-lookup"><span data-stu-id="e313b-143">Text Services Framework Correction User Interface</span></span>

<span data-ttu-id="e313b-144">Dans cet exemple, tous les champs d’entrée sont des contrôles [InkEdit](/previous-versions/ms552265(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="e313b-144">In this sample all of the input fields are [InkEdit](/previous-versions/ms552265(v=vs.100)) controls.</span></span> <span data-ttu-id="e313b-145">Cela est important, car le contrôle InkEdit intègre une prise en charge de [Text Services Framework](../tsf/text-services-framework.md) (TSF) et peut donc prendre en charge l’interface utilisateur de correction sur place pour les entrées reçues de l’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="e313b-145">This is significant because the InkEdit control has built-in support for the [Text Services Framework](../tsf/text-services-framework.md) (TSF) and is thus capable of supporting the in-place correction user interface for input received from the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object.</span></span>

<span data-ttu-id="e313b-146">La valeur par défaut de [EnableTsf](/previous-versions/ms569656(v=vs.100)) est **true**.</span><span class="sxs-lookup"><span data-stu-id="e313b-146">The default value for [EnableTsf](/previous-versions/ms569656(v=vs.100)) is **TRUE**.</span></span> <span data-ttu-id="e313b-147">L’objet [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) tente alors de démarrer Text Services Framework (TSF) sur le contrôle attaché.</span><span class="sxs-lookup"><span data-stu-id="e313b-147">This causes the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to attempt to start the Text Services Framework (TSF) on the attached control.</span></span> <span data-ttu-id="e313b-148">En cas de réussite, l’interface utilisateur de correction apparaît dans le contrôle et permet l’accès aux alternatives de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="e313b-148">If successful, the correction user interface shows in the control, and it allows access to recognition alternates.</span></span> <span data-ttu-id="e313b-149">L’appel de cette méthode avec un paramètre **false** tente d’arrêter TSF sur le contrôle attaché.</span><span class="sxs-lookup"><span data-stu-id="e313b-149">Calling this method with a **FALSE** parameter attempts to shut down TSF on the attached control.</span></span>

<span data-ttu-id="e313b-150">Le contrôle [InkEdit](/previous-versions/ms552265(v=vs.100)) fournit déjà une interface utilisateur de correction, mais dans l’exemple [EnableTsf](/previous-versions/ms569656(v=vs.100)) est utilisé pour permettre à [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) d’utiliser le contexte du module de reconnaissance d’insertion TSF plutôt que la fonction [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) pour envoyer les résultats de reconnaissance de l’écriture manuscrite dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="e313b-150">The [InkEdit](/previous-versions/ms552265(v=vs.100)) control already provides a correction user interface, but in the sample [EnableTsf](/previous-versions/ms569656(v=vs.100)) is used to enable the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) to use the TSF insertion recognizer context rather than the [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) function to send the handwriting recognition results into the control.</span></span> <span data-ttu-id="e313b-151">Le résultat est que du texte peut être inséré même si le champ n’a plus le focus.</span><span class="sxs-lookup"><span data-stu-id="e313b-151">The result is that text can be inserted even if the field no longer has focus.</span></span>


```C++
  pipName.EnableTsf(true);
  pipPolicyNumber.EnableTsf(true);
```



## <a name="closing-the-form"></a><span data-ttu-id="e313b-152">Fermeture du formulaire</span><span class="sxs-lookup"><span data-stu-id="e313b-152">Closing the Form</span></span>

<span data-ttu-id="e313b-153">Dans le code généré par le Concepteur Windows Form, les contrôles [InkEdit](/previous-versions/ms552265(v=vs.100)) et [InkPicture](/previous-versions/aa514604(v=msdn.10)) sont ajoutés à la liste des composants du formulaire lorsque le formulaire est initialisé.</span><span class="sxs-lookup"><span data-stu-id="e313b-153">In the Windows Form Designer generated code, the [InkEdit](/previous-versions/ms552265(v=vs.100)) and [InkPicture](/previous-versions/aa514604(v=msdn.10)) controls are added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="e313b-154">Lorsque le formulaire se ferme, les contrôles InkEdit et InkPicture sont supprimés, ainsi que les autres composants du formulaire, par la méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) du formulaire.</span><span class="sxs-lookup"><span data-stu-id="e313b-154">When the form closes, the InkEdit and InkPicture controls are disposed, as well as the other components of the form, by the form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method.</span></span> <span data-ttu-id="e313b-155">La méthode dispose du formulaire supprime également les objets [Ink](/previous-versions/aa515768(v=msdn.10)) créés pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="e313b-155">The form's Dispose method also disposes the [Ink](/previous-versions/aa515768(v=msdn.10)) objects that are created for the form.</span></span>

 

 
