---
description: Cette section explique comment récupérer le balisage MathML à partir du contrôle d’entrée mathématique à l’aide de l’Active Template Library (ATL) et du modèle COM (Component Object Model).
ms.assetid: 352d2a0c-8275-4fe4-b523-4c74126ffadf
title: Réception d’une entrée du contrôle d’entrée mathématique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 830c8f57bb7b27c305928cf68b658dcc37ede5d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534746"
---
# <a name="receiving-input-from-the-math-input-control"></a><span data-ttu-id="38d02-103">Réception d’une entrée du contrôle d’entrée mathématique</span><span class="sxs-lookup"><span data-stu-id="38d02-103">Receiving Input from the Math Input Control</span></span>

<span data-ttu-id="38d02-104">Cette section explique comment récupérer le balisage MathML à partir du contrôle d’entrée mathématique à l’aide de l’Active Template Library (ATL) et du modèle COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="38d02-104">This section explains how to retrieve the MathML markup from the math input control using the Active Template Library (ATL) and the Component Object Model (COM).</span></span>

<span data-ttu-id="38d02-105">Pour récupérer l’équation mathématique reconnue à partir du contrôle d’entrée mathématique, vous pouvez remplacer le comportement qui se produit lorsque vous appuyez sur le bouton d’insertion.</span><span class="sxs-lookup"><span data-stu-id="38d02-105">To retrieve the recognized math equation from the math input control, you can override the behavior that happens when the insert button is pressed.</span></span> <span data-ttu-id="38d02-106">Pour ce faire, vous devez configurer un gestionnaire d’événements qui implémente les différents événements pris en charge par l’interface [**\_ IMathInputControlEvents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) .</span><span class="sxs-lookup"><span data-stu-id="38d02-106">To do this, you will need to set up an event handler that implements the various events that are supported by the [**\_IMathInputControlEvents**](/windows/win32/api/micaut/nn-micaut-_imathinputcontrolevents) interface.</span></span> <span data-ttu-id="38d02-107">La configuration du gestionnaire d’événements implique la réalisation des étapes suivantes pour les événements que vous souhaitez prendre en charge (Insert dans ce cas).</span><span class="sxs-lookup"><span data-stu-id="38d02-107">Setting up the events handler involves the performing the following steps for the events you want to support (insert in this case).</span></span>

-   [<span data-ttu-id="38d02-108">Créer une classe de modèle qui contient des récepteurs d’événements</span><span class="sxs-lookup"><span data-stu-id="38d02-108">Create a template class that contains event sinks</span></span>](#create-a-template-class-that-contains-event-sinks)
-   [<span data-ttu-id="38d02-109">Configurer les gestionnaires d’événements</span><span class="sxs-lookup"><span data-stu-id="38d02-109">Set up the event handlers</span></span>](#set-up-the-event-handlers)
-   [<span data-ttu-id="38d02-110">Hériter de la classe de gestionnaire d’événements dans votre classe principale</span><span class="sxs-lookup"><span data-stu-id="38d02-110">Inherit the event handler class in your main class</span></span>](#inherit-the-event-handler-class-in-your-main-class)
-   [<span data-ttu-id="38d02-111">Initialiser votre classe pour hériter du ou des récepteurs d’événements</span><span class="sxs-lookup"><span data-stu-id="38d02-111">Initialize your class to inherit the event sink(s)</span></span>](#initialize-your-class-to-inherit-the-event-sinks)

## <a name="create-a-template-class-that-contains-event-sinks"></a><span data-ttu-id="38d02-112">Créer une classe de modèle qui contient des récepteurs d’événements</span><span class="sxs-lookup"><span data-stu-id="38d02-112">Create a template class that contains event sinks</span></span>

<span data-ttu-id="38d02-113">Lorsque vous implémentez un récepteur d’événements qui utilise le contrôle d’entrée mathématique, vous devez d’abord spécifier un ID de récepteur. Vous devez ensuite créer une classe de modèle qui hérite de l’événement, du gestionnaire de contrôle d’événements et des interfaces d’événements de contrôle d’entrée mathématique.</span><span class="sxs-lookup"><span data-stu-id="38d02-113">When you are implementing an event sink that uses the math input control, you must first specify a sink id. You must then create a template class that inherits from the event, event control handler, and math input control event interfaces.</span></span> <span data-ttu-id="38d02-114">Le code suivant montre comment définir un ID de récepteur et créer une telle classe de modèle, CMathInputControlEventHandler, qui hérite des interfaces requises.</span><span class="sxs-lookup"><span data-stu-id="38d02-114">The following code shows how to set a sink id and create such a template class, CMathInputControlEventHandler, that inherits from the requisite interfaces.</span></span> <span data-ttu-id="38d02-115">Cette classe de modèle est également configurée pour avoir un pointeur d’interface inconnu privé qui sera utilisé pour passer le contrôle d’entrée mathématique à celle-ci lors de l’initialisation et le \_ membre m ulAdviseCount pour compter le nombre d’appels à Advise/Unadvise.</span><span class="sxs-lookup"><span data-stu-id="38d02-115">This template class also is set up to have a private unknown interface pointer that will be used to pass the math input control to it on initialization and the m\_ulAdviseCount member to count the number of calls to advise / unadvise.</span></span>


```
  
#pragma once
static const int MATHINPUTCONTROL_SINK_ID = 1 ;

template <class T>
class ATL_NO_VTABLE CMathInputControlEventHandler :
    public IDispEventSimpleImpl<MATHINPUTCONTROL_SINK_ID, CMathInputControlEventHandler<T>, &__uuidof(_IMathInputControlEvents)>
{
private:
    IUnknown    *m_pUnknown;
    ULONG m_ulAdviseCount;
    CDialog *m_pMain;

```



> [!Note]  
> <span data-ttu-id="38d02-116">Le membre **m \_ pMain** doit être différent dans votre implémentation si vous n’utilisez pas de dialogue.</span><span class="sxs-lookup"><span data-stu-id="38d02-116">The member **m\_pMain** should be different in your implementation if you are not using a dialog.</span></span>

 

<span data-ttu-id="38d02-117">Maintenant que vous disposez de la classe de modèle de base, vous devez fournir une déclaration anticipée pour les gestionnaires d’événements que vous allez remplacer et configurer ensuite une table de récepteurs pour les événements que vous allez gérer.</span><span class="sxs-lookup"><span data-stu-id="38d02-117">Now that you have the basic template class, you must give a forward declaration for the event handlers that you will be overriding and must then set up a sink map for the events you will be handling.</span></span> <span data-ttu-id="38d02-118">Le code suivant montre comment configurer des gestionnaires d’événements pour la méthode [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) , appelée lorsqu’un utilisateur clique sur le bouton Insérer dans le contrôle d’entrée mathématique, et la méthode [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) , appelée lorsqu’un utilisateur clique sur le bouton Annuler dans le contrôle d’entrée mathématique.</span><span class="sxs-lookup"><span data-stu-id="38d02-118">The following code shows how to set up event handlers for the [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) method, called when a user clicks the insert button on the math input control, and the [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) method, called when a user clicks the cancel button on the math input control.</span></span>


```
  
public:
    static const _ATL_FUNC_INFO OnMICInsertInfo; // = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
    static const _ATL_FUNC_INFO OnMICCloseInfo;  // = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

    BEGIN_SINK_MAP(CMathInputControlEventHandler)
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICInsert, OnMICInsert, const_cast<_ATL_FUNC_INFO*>(&OnMICInsertInfo))
        SINK_ENTRY_INFO(MATHINPUTCONTROL_SINK_ID, __uuidof(_IMathInputControlEvents), DISPID_MICClose, OnMICClose, const_cast<_ATL_FUNC_INFO*>(&OnMICCloseInfo))  
    END_SINK_MAP()
```



<span data-ttu-id="38d02-119">Étant donné que vous allez utiliser le contrôle d’entrée mathématique, il est utile de définir une référence interne à l’interface appropriée.</span><span class="sxs-lookup"><span data-stu-id="38d02-119">Since you will be working with the math input control, it will be useful to set an internal reference to the relevant interface.</span></span> <span data-ttu-id="38d02-120">La fonction utilitaire suivante est créée dans l’exemple de classe pour définir cette référence.</span><span class="sxs-lookup"><span data-stu-id="38d02-120">The following utility function is created in the example class to set this reference.</span></span>


```
    
  HRESULT Initialize(IUnknown *pUnknown, CDialog *pMain)
  {
    m_pMain  = pMain;
    m_pUnknown = pUnknown;
    m_ulAdviseCount = 0;
    return S_OK;
  }
  
```



## <a name="set-up-the-event-handlers"></a><span data-ttu-id="38d02-121">Configurer les gestionnaires d’événements</span><span class="sxs-lookup"><span data-stu-id="38d02-121">Set up the event handlers</span></span>

<span data-ttu-id="38d02-122">Une fois que vous avez configuré les récepteurs d’événements, vous devez créer vos implémentations des récepteurs d’événements.</span><span class="sxs-lookup"><span data-stu-id="38d02-122">Once you have set up the event sinks, you will need to create your implementations of the event sinks.</span></span> <span data-ttu-id="38d02-123">Dans les deux méthodes de l’exemple de code suivant, les récepteurs d’événements récupèrent un descripteur de l’interface de contrôle d’entrée mathématique.</span><span class="sxs-lookup"><span data-stu-id="38d02-123">In both of the methods in the following code example, the event sinks retrieve a handle to the math input control interface.</span></span> <span data-ttu-id="38d02-124">Dans la fonction [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) , le résultat de la reconnaissance est affiché en tant que MathML et le contrôle est masqué.</span><span class="sxs-lookup"><span data-stu-id="38d02-124">In the [**Insert**](/previous-versions/windows/desktop/legacy/dd317352(v=vs.85)) function, the recognition result is displayed as MathML and the control is hidden.</span></span> <span data-ttu-id="38d02-125">Dans la fonction [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) , le contrôle d’entrée mathématique est masqué.</span><span class="sxs-lookup"><span data-stu-id="38d02-125">In the [**Close**](/previous-versions/windows/desktop/legacy/dd317351(v=vs.85)) function, the math input control is hidden.</span></span>


```
  
    // Methods
    HRESULT __stdcall OnMICInsert( BSTR bstrRecoResult)
    {
        CComQIPtr<IMathInputControl> spMIC(m_pUnknown);
        HRESULT hr=S_OK;
        if (spMIC)
        {           
            MessageBox(NULL,bstrRecoResult,L"Recognition Result",MB_OK);
            hr = spMIC->Hide();
            return hr;  
        }
        return E_FAIL;          
    }

    HRESULT __stdcall OnMICClose()
    {
        CComPtr<IMathInputControl> spMIC;
        HRESULT hr = m_pUnknown->QueryInterface<IMathInputControl>(&spMIC);
        if (SUCCEEDED(hr))
        {           
            hr = spMIC->Hide();
            return hr;  
        }
        return hr;                  
    }
};  
```



## <a name="inherit-the-event-handler-class-in-your-main-class"></a><span data-ttu-id="38d02-126">Hériter de la classe de gestionnaire d’événements dans votre classe principale</span><span class="sxs-lookup"><span data-stu-id="38d02-126">Inherit the event handler class in your main class</span></span>

<span data-ttu-id="38d02-127">Une fois que votre classe de modèle est implémentée, vous devez l’hériter de la classe dans laquelle vous allez configurer votre contrôle d’entrée mathématique.</span><span class="sxs-lookup"><span data-stu-id="38d02-127">After you have your template class implemented, you will need to inherit it into the class that you will be setting up your math input control in.</span></span> <span data-ttu-id="38d02-128">Dans le cadre de ce guide, cette classe est une boîte de dialogue, CMIC \_ test \_ EVENTSDlg.</span><span class="sxs-lookup"><span data-stu-id="38d02-128">For the purposes of this guide, this class is a dialog, CMIC\_TEST\_EVENTSDlg.</span></span> <span data-ttu-id="38d02-129">Dans l’en-tête de boîte de dialogue, les en-têtes nécessaires doivent être inclus et la classe de modèle que vous avez créée doit être héritée.</span><span class="sxs-lookup"><span data-stu-id="38d02-129">In the dialog header, the requisite headers must be included and the template class you created must be inherited.</span></span> <span data-ttu-id="38d02-130">La classe à laquelle vous héritez et les gestionnaires d’événements doivent avoir des déclarations anticipées afin que le modèle puisse être implémenté.</span><span class="sxs-lookup"><span data-stu-id="38d02-130">The class you're inheriting within and the event handlers must have forward declarations so that the template can be implemented.</span></span> <span data-ttu-id="38d02-131">L’exemple de code suivant montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="38d02-131">The following code example shows how this is done.</span></span>


```
#pragma once
#include <atlbase.h>
#include <atlwin.h>

// include for MIC
#include "micaut.h"

// include for event sinks
#include <iacom.h>
#include "mathinputcontroleventhandler.h"

class CMIC_TEST_EVENTSDlg;

const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICInsertInfo = {CC_STDCALL, VT_I4, 1, {VT_BSTR}};
const _ATL_FUNC_INFO CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::OnMICCloseInfo = {CC_STDCALL, VT_I4, 0, {VT_EMPTY}};

// CMIC_TEST_EVENTSDlg dialog
class CMIC_TEST_EVENTSDlg : public CDialog,
    public CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>
{
  public:
  CComPtr<IMathInputControl> m_spMIC; // Math Input Control

  
```



> [!Note]  
> <span data-ttu-id="38d02-132">Le type de modèle, **Cmic \_ test \_ EventsDlg**, sera différent, sauf si vous avez nommé votre classe comme dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="38d02-132">The template type, **CMIC\_TEST\_EventsDlg**, will be different unless you have named your class the same as the example.</span></span>

 

## <a name="initialize-your-class-to-inherit-the-event-sinks"></a><span data-ttu-id="38d02-133">Initialiser votre classe pour hériter du ou des récepteurs d’événements</span><span class="sxs-lookup"><span data-stu-id="38d02-133">Initialize your class to inherit the event sink(s)</span></span>

<span data-ttu-id="38d02-134">Une fois que vous avez configuré votre classe de sorte qu’elle hérite de la classe de modèle, vous êtes prêt à la configurer pour gérer les événements.</span><span class="sxs-lookup"><span data-stu-id="38d02-134">Once you have set up your class to inherit from the template class, you are ready to set it up to handle events.</span></span> <span data-ttu-id="38d02-135">Cela consiste à initialiser la classe pour avoir un handle vers le contrôle d’entrée mathématique et la classe appelante.</span><span class="sxs-lookup"><span data-stu-id="38d02-135">This will consist of initializing the class to have a handle to the math input control and the calling class.</span></span> <span data-ttu-id="38d02-136">En outre, le contrôle d’entrée mathématique pour gérer les événements de doit être envoyé à la méthode DispEventAdvise qui hérite de la classe d’exemple CMathInputControlEventHandler.</span><span class="sxs-lookup"><span data-stu-id="38d02-136">Additionally, the math input control to handle events from must be sent to the DispEventAdvise method that the CMathInputControlEventHandler example class inherits.</span></span> <span data-ttu-id="38d02-137">Le code suivant est appelé à partir de la méthode OnInitDialog dans l’exemple de classe pour effectuer ces actions.</span><span class="sxs-lookup"><span data-stu-id="38d02-137">The following code is called from the OnInitDialog method in the example class to perform these actions.</span></span>


```
// includes for implementation
#include "micaut_i.c"

// include for event handler
#include "mathinputcontroleventhandler.h"

...

OnInitDialog{
  ...

  // TODO: Add extra initialization here
  CoInitialize(NULL);
  HRESULT hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
  if (SUCCEEDED(hr)){
    hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::Initialize(m_spMIC, this);
      if (SUCCEEDED(hr)){
        hr = CMathInputControlEventHandler<CMIC_TEST_EVENTSDlg>::DispEventAdvise(m_spMIC);            
        if (SUCCEEDED(hr)){
          hr = m_spMIC->Show();  
        }
      }
    }
  }  
}
  
```



> [!Note]  
> <span data-ttu-id="38d02-138">Le type de modèle, CMIC \_ test \_ EventsDlg dans cet exemple, sera différent, sauf si vous avez nommé votre classe comme dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="38d02-138">The template type, CMIC\_TEST\_EventsDlg in this example, will be different unless you have named your class the same as the example.</span></span>

 

 

 
