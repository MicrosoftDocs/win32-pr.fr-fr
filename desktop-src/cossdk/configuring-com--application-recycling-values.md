---
description: Vous pouvez utiliser les méthodes suivantes pour configurer les valeurs de recyclage d’applications pour votre application COM+.
ms.assetid: 8f6a4879-cf4c-4171-8448-bc07371e038c
title: Configuration des valeurs de recyclage des applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2613fb6f063a49d53baa90fad6f7dac862b848c6abf95fddcc36ace25e3d6b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548640"
---
# <a name="configuring-com-application-recycling-values"></a>Configuration des valeurs de recyclage des applications COM+

Vous pouvez utiliser les méthodes suivantes pour configurer les valeurs de recyclage d’applications pour votre application COM+.

> [!Note]  
> vous ne pouvez pas recycler une application COM+ qui a été configurée pour s’exécuter en tant que service Windows. En outre, les applications de bibliothèque disposent des propriétés de recyclage et de regroupement de leur processus hôte.

 

## <a name="component-services-administrative-tool"></a>Outil d’administration Services de composants

Pour configurer le recyclage d’applications pour une application COM+, procédez comme suit :

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, cliquez avec le bouton droit sur l’application serveur COM+ que vous souhaitez recycler, puis cliquez sur **Propriétés**.

2.  Dans l’onglet **regroupement & recyclage** , entrez des valeurs pour **limite de durée de vie (minutes)**, **limite de mémoire (Ko)**, **délai d’expiration (minutes)**, **limite d’appel** et **limite d’activation**, en fonction des critères que vous souhaitez utiliser.

    -   **Limite de durée de vie** indique le nombre maximal de minutes pendant lesquelles un processus peut s’exécuter avant son recyclage. La plage valide est comprise entre 0 et 30 240 minutes (21 jours). Le nombre de minutes par défaut est 0.
    -   La **limite de mémoire** indique la quantité maximale d’utilisation de la mémoire de processus (en kilo-octets) avant le recyclage du processus. Si l’utilisation de la mémoire du processus dépasse le nombre spécifié pendant plus d’une minute, le processus est recyclé. La plage valide est comprise entre 0 et 1 048 576 Ko, et la quantité d’utilisation de la mémoire par défaut est de 0 Ko.
    -   **Délai d’expiration** indique le nombre de minutes à attendre, avant d’être arrêté de force, pour la libération de toutes les références externes aux objets du processus. La plage valide est comprise entre 1 et 1440 minutes (24 heures) et le délai d’expiration par défaut est de 15 minutes. Cette valeur est utilisée uniquement lorsqu’il est déjà déterminé qu’un processus sera recyclé selon les autres critères.
    -   **Limite d’appel** indique le nombre maximal d’appels que les objets d’application peuvent accepter avant de recycler le processus. La plage valide est comprise entre 0 et 1 048 576 appels, et le nombre d’appels par défaut est 0.
    -   **Limite d’activation** indique le nombre maximal d’activations d’objets d’application à accepter avant de recycler le processus. La plage valide est comprise entre 0 et 1 048 576 activations, et le nombre d’activations par défaut est 0.

    > [!Note]  
    > Lorsque la limite de **durée de vie**, la limite de **mémoire**, la **limite d’appel** ou la valeur de limite d' **activation** est définie sur 0 (valeur par défaut), le recyclage d’applications pour ce critère est désactivé. Lorsque les quatre critères ont la valeur 0, le recyclage de l’application est désactivé pour l’application sélectionnée.

     

3.  Cliquez sur **OK**.

## <a name="visual-basic"></a>Visual Basic

la fonction suivante dans Microsoft Visual Basic montre comment vous pouvez définir les valeurs de recyclage d’application pour n’importe quelle application serveur COM+ que vous choisissez. pour l’utiliser à partir de Visual Basic, ajoutez une référence à la bibliothèque de types d’administration COM+.


```VB
Function SetMyApplicationRecycling( _
  strApplicationName As String, _
  lngLifetimeLimit As Long, _
  lngMemoryLimit As Long, _
  lngCallLimit As Long, _
  lngActivationLimit As Long, _
  lngExpirationTimeout As Long _
) As Boolean  ' Return False if any errors occur.

    SetMyApplicationRecycling = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim objCatalog As COMAdmin.COMAdminCatalog
    Dim objAppCollection As COMAdmin.COMAdminCatalogCollection
    Dim objApplication As COMAdmin.COMAdminCatalogObject
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objAppCollection = objCatalog.GetCollection("Applications")
    objAppCollection.Populate
    For Each objApplication In objAppCollection
        With objApplication
            If .Name = strApplicationName Then
                .Value("RecycleLifetimeLimit") = lngLifetimeLimit
                .Value("RecycleMemoryLimit") = lngMemoryLimit
                .Value("RecycleCallLimit") = lngCallLimit
                .Value("RecycleActivationLimit") = lngActivationLimit
                .Value("RecycleExpirationTimeout") = lngExpirationTimeout
                MsgBox strApplicationName & _
                  " recycling values are now set to the following: " & _
                  vbNewLine & vbNewLine & _
                  "Lifetime Limit = " & lngLifetimeLimit & vbNewLine & _
                  "Memory Limit = " & lngMemoryLimit & vbNewLine & _
                  "Call Limit = " & lngCallLimit & vbNewLine & _
                  "Activation Limit = " & lngActivationLimit & vbNewLine _
                  & "Expiration Timeout = " & lngExpirationTimeout
                Exit For
            End If
        End With
    Next
    objAppCollection.SaveChanges
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
    SetMyApplicationRecycling = True  ' Successful end to procedure
    Exit Function
    
My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
End Function

```



Pour utiliser la fonction, fournissez une valeur de chaîne pour le nom de l’application et les valeurs entières pour les paramètres de recyclage d’application souhaités. le code Visual Basic suivant montre comment définir la valeur **RecycleLifetimeLimit** sur 5, la valeur **RecycleMemoryLimit** sur 10, la valeur **RecycleCallLimit** sur 9, la valeur **RecycleActivationLimit** sur 100 et la valeur **RecycleExpirationTimeout** sur 15.


```VB
Sub Main()
    If Not SetMyApplicationRecycling("MyApp", 5, 10, 9, 100, 15) Then
        MsgBox "SetMyApplicationRecycling failed."
    End If
End Sub

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de recyclage des applications COM+](com--application-recycling-concepts.md)
</dt> </dl>

 

 



