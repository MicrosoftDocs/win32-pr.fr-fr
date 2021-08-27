---
title: Windows Gestes tactiles dans l’exemple C (MTGesturesCS)
description: cette section décrit l’exemple de gestes tactiles Windows dans C \.
ms.assetid: 4b2d70bb-47e4-4448-97e2-6f6e29d1dfdf
keywords:
- Windows Touch, exemples de code
- Windows Toucher, exemple de code
- Windows Toucher, mouvements
- Windows Toucher, exemples de geste
- Exemples de mouvements
- gestes, exemple de code
- mouvements, exemples de code
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: ac3a7c0772ad7329d14d9909b55f8a60ef6e7d7473a06fcba921297117a00b6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089902"
---
# <a name="windows-touch-gestures-in-c-sample-mtgesturescs"></a>Windows Gestes tactiles dans l’exemple C# (MTGesturesCS)

cette section décrit l’exemple de gestes tactiles Windows en C#.

cet exemple Windows les gestes tactiles montre comment utiliser des messages de mouvement pour translater, faire pivoter et mettre à l’échelle une zone rendue par le Graphics Device Interface (GDI) en gérant le message d' [**WM_GESTURE**](wm-gesture.md) . La capture d’écran suivante montre comment l’exemple apparaît lorsqu’il est en cours d’exécution.

![capture d’écran montrant les gestes tactiles Windows dans l’échantillon net Sharp lorsqu’il est en cours d’exécution, avec un rectangle blanc avec contour noir centré à l’écran](images/mtgesturescs.png)

Pour cet exemple, les messages de mouvement sont passés à un moteur de mouvement qui appelle ensuite des méthodes sur des objets de dessin pour translater, faire pivoter et mettre à l’échelle un objet qui a des méthodes pour gérer ces commandes. Pour que cela soit possible en C#, une forme spéciale, TouchableForm, est créée pour gérer les messages de mouvement. ce formulaire utilise ensuite les messages pour apporter des modifications à un objet de dessin, DrawingObject, pour modifier le rendu de l’objet dans la méthode Paint.

Pour vous aider à voir comment fonctionne l’exemple, examinez les étapes d’utilisation de la commande PAN pour traduire la zone rendue. Un utilisateur effectue le mouvement de panoramique qui génère un message de [**WM_GESTURE**](wm-gesture.md) avec l’identificateur de mouvement GID_PAN. Le TouchableForm gère ces messages et met à jour la position de l’objet de dessin, et l’objet est ensuite rendu traduit.

Le code suivant montre comment le gestionnaire de mouvements récupère les paramètres du message [**WM_GESTURE**](wm-gesture.md) , puis effectue la traduction sur la zone rendue via un appel à la méthode Move de l’objet Drawing.

```CSharp
            switch (gi.dwID)
            {
                case GID_BEGIN:
                case GID_END:
                    break;
               (...)
                case GID_PAN:
                    switch (gi.dwFlags)
                    {
                        case GF_BEGIN:
                            _ptFirst.X = gi.ptsLocation.x;
                            _ptFirst.Y = gi.ptsLocation.y;
                            _ptFirst = PointToClient(_ptFirst);
                            break;

                        default:
                            // We read the second point of this gesture. It is a
                            // middle point between fingers in this new position
                            _ptSecond.X = gi.ptsLocation.x;
                            _ptSecond.Y = gi.ptsLocation.y;
                            _ptSecond = PointToClient(_ptSecond);

                            // We apply move operation of the object
                            _dwo.Move(_ptSecond.X - _ptFirst.X, _ptSecond.Y - _ptFirst.Y);

                            Invalidate();

                            // We have to copy second point into first one to
                            // prepare for the next step of this gesture.
                            _ptFirst = _ptSecond;
                            break;
                    }
                    break;
```

Le code suivant montre comment la méthode Move de l’objet de dessin met à jour les variables de position internes.

```CSharp
        public void Move(int deltaX,int deltaY)
        {
            _ptCenter.X += deltaX;
            _ptCenter.Y += deltaY;
        }
```

Le code suivant montre comment la position est utilisée dans la méthode Paint de l’objet Drawing.

```CSharp
public void Paint(Graphics graphics)
        {
(...)
            for (int j = 0; j < 5; j++)
            {
                int idx = arrPts[j].X;
                int idy = arrPts[j].Y;

                // rotation
                arrPts[j].X = (int)(idx * dCos + idy * dSin);
                arrPts[j].Y = (int)(idy * dCos - idx * dSin);

                // translation
                arrPts[j].X += _ptCenter.X;
                arrPts[j].Y += _ptCenter.Y;
            }
(...)
        }
```

Les gestes panoramiques entraînent le rendu de la zone dessinée.

## <a name="related-topics"></a>Rubriques connexes

[application de mouvements tactiles multiples (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [application de gestes multipoint (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), exemples de [touches tactiles Windows](windows-touch-samples.md)
