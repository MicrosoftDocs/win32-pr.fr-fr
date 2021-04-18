---
description: Le &\# 0034 ; compartiment à fuite&\# 0034 ; le modèle est un moyen de modéliser les exigences de mise en mémoire tampon pour une lecture fluide.
ms.assetid: 2f7f80d6-3abb-462f-a571-b223a1d59da6
title: Modèle de mémoire tampon de compartiment avec fuite (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5a99932fb121808f6a49323360c47c09d0acbb
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106520246"
---
# <a name="the-leaky-bucket-buffer-model-microsoft-media-foundation"></a>Modèle de mémoire tampon de compartiment avec fuite (Microsoft Media Foundation)

Lorsque vous diffusez du contenu multimédia sur un réseau, le décodeur reçoit des données encodées à un taux théoriquement constant (vitesse de transmission). Le décodeur utilise ces données pour produire une sortie décodée. Toutefois, dans le cas général, le décodeur consomme les données à une vitesse *variable* , car l’encodeur peut utiliser un taux d’encodage variable.

Le modèle « compartiment perdu » est un moyen de modéliser les exigences de mise en mémoire tampon pour une lecture en douceur. Dans ce modèle, le décodeur gère une mémoire tampon. Les données encodées passent du réseau dans la mémoire tampon et de la mémoire tampon dans le décodeur. Si la mémoire tampon est dépassée, cela signifie que le décodeur supprime les données de la mémoire tampon plus rapidement que le réseau ne les fournit. En cas de dépassement de la mémoire tampon, cela signifie que le réseau fournit des données plus rapidement que le décodeur ne l’utilise.

Cette rubrique décrit le modèle de « compartiment perdu » de mémoires tampons pour l’encodage et le décodage.

-   [Le compartiment avec fuite](#the-leaky-bucket)
-   [Le compartiment en cours d’utilisation](#the-bucket-in-use)
-   [Définition des valeurs de compartiment fuites pour les flux ASF](#setting-leaky-bucket-values-for-asf-streams)
-   [Valeurs de compartiment avec fuite dans le multiplexeur ASF](#leaky-bucket-values-in-the-asf-multiplexer)
-   [Mise à jour des valeurs de compartiment avec fuite dans le récepteur de média ASF](#updating-leaky-bucket-values-in-the-asf-media-sink)
-   [Rubriques connexes](#related-topics)

## <a name="the-leaky-bucket"></a>Le compartiment avec fuite

Pour comprendre le modèle de compartiments avec fuite, envisagez un compartiment avec un petit trou en bas. Trois paramètres définissent le compartiment :

-   La capacité (B)
-   Vitesse à laquelle le flux d’eau sort du compartiment (R)
-   Remplissage initial du compartiment (F)

Dans cette métaphore, le compartiment est le tampon :

![Illustration montrant une mémoire tampon en tant que compartiment, taux d’entrée pour l’entrée d’eau dans le compartiment et vitesse de sortie en tant qu’eau quittant un trou dans le compartiment](images/asf-components03.png)

Si l’eau est dans le compartiment au taux exact *R*, le compartiment restera à F, car le taux d’entrée est égal au taux de sortie. Si la vitesse d’entrée augmente alors que *R* reste constant, le compartiment accumule de l’eau. Si la vitesse d’entrée est supérieure à *R* pendant une période prolongée, le compartiment finit par dépasser. Toutefois, le taux d’entrée peut varier de *R* sans déborder le compartiment, tant que la vitesse d’entrée moyenne ne dépasse pas la capacité du compartiment. Plus la capacité est grande, plus le taux d’entrée peut varier dans une fenêtre de temps donnée.

En ASF, le compartiment avec fuite est défini par trois paramètres :

-   Vitesse de transmission moyenne, en octets par seconde, qui correspond au taux de sortie (*R*)
-   Fenêtre de mémoire tampon, mesurée en millisecondes, qui correspond à la capacité de compartiment (*B*).
-   La saturation de la mémoire tampon initiale, qui est généralement définie à zéro.

La vitesse de transmission mesure le nombre moyen de bits par seconde dans le flux encodé. La fenêtre de mémoire tampon mesure le nombre de millisecondes de données à la vitesse de transmission qui peut tenir dans la mémoire tampon. La taille de la mémoire tampon en bits est égale à R \* (B/1000).

Les données de charge utile ASF peuvent entrer dans le compartiment présentant des fuites à des moments irréguliers et en quantités irrégulières, mais doivent laisser le compartiment à une vitesse de transmission positive constante. En raison de la fenêtre de mémoire tampon, il existe un délai entre le moment où la charge utile entre dans le compartiment et le moment où elle sort. Le délai maximal qui peut se produire est de *B* / *R*. Les données de charge utile qui entrent dans le compartiment sont en fonction de l’heure de présentation et ne doivent jamais dépasser le compartiment. Outre l’heure de la présentation, chaque charge utile a également un temps d’envoi, c’est-à-dire l’heure à laquelle les données de la charge utile quittent le compartiment en fonction de la vitesse de transmission. L’heure d’envoi doit être antérieure à l’heure de la présentation pour garantir que, lorsque le compartiment de fuite est proche de plein, chaque charge utile quitte le compartiment avant ou pendant sa présentation. Pour ce faire, les durées de présentation sont décalées par rapport à la valeur *B* / *R* (le *préroll*) et les heures d’envoi commencent à zéro. L’heure d’envoi ne doit pas être postérieure à l’heure de la présentation, car cela indiquerait que la charge utile entrée dans le compartiment est trop tardive et ne peut pas être incluse dans l’objet de données. La valeur du préroll est incluse dans l' [objet d’en-tête ASF](asf-file-structure.md) .

Pour la diffusion en continu sans problème sur le réseau, les flux compressés dans le contenu du média doivent conserver une vitesse de transmission constante pendant toute la durée de la lecture. Le modèle de compartiment présentant des fuites ASF garantit que les données multimédias sont envoyées sur le réseau à une vitesse de transmission constante. Les paramètres du compartiment avec fuite sont spécifiés dans l’objet de propriétés de flux étendu de l' [objet d’en-tête ASF](asf-file-structure.md). Dans Microsoft Media Foundation, ils sont définis en tant qu’attributs sur le type de média qui représente le flux.

Les valeurs des compartiments de fuites sont définies dans le récepteur de fichiers ASF et l’objet multiplexeur ASF sous-jacent, et l’encodeur Windows Media. Ces valeurs peuvent être identiques ou différentes. Prenons l’exemple d’un scénario de diffusion en continu, qui requiert la livraison des échantillons audio plus tard que les exemples de vidéos afin que le fichier puisse être diffusé en continu sans latence. Pour ce faire, le compartiment fuite du flux audio dans le récepteur multimédia peut être défini sur une valeur supérieure à la valeur définie dans l’encodeur audio Windows Media.

Pour définir des valeurs B/R dans l’encodeur, l’application doit définir les propriétés [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md), [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md), [**MFPKEY \_ Rmax**](mfpkey-rmaxproperty.md)et [**MFPKEY BMAX. \_**](mfpkey-bmaxproperty.md) Pour plus d’informations sur la définition des propriétés dans l’encodeur, consultez [Propriétés de codage](configuring-the-encoder.md).

## <a name="the-bucket-in-use"></a>Le compartiment en cours d’utilisation

L’objectif d’un encodeur est de s’assurer que le contenu ne dépasse jamais la mémoire tampon. L’encodeur utilise les valeurs de la vitesse de transmission et de la fenêtre de mémoire tampon comme guides. Le nombre réel de bits transmis sur une période de temps égale à la fenêtre de mémoire tampon ne peut jamais être supérieur à deux fois la taille de la mémoire tampon.

Prenons l’exemple suivant : vous avez un compartiment à 3 litres avec un trou dans lequel 1 litre peut circuler par minute. Vous placez le compartiment sous un emboîtement et ouvrez la vanne pour laisser l’eau à un taux de 1 gallon par minute. L’eau sort du compartiment aussi rapidement qu’elle entre, sans aucun supplément dans le compartiment. Vous augmentez ensuite le passage de l’emboîtement à 2 litres par minute. Chaque minute, le flux de l’eau atteint ce débit, 2 gallons entrent dans le compartiment et 1 litre de fuites, laissant 1 litre dans le compartiment. À la fin de 3 minutes, 6 gallons d’eau sont allés dans le compartiment, 3 gallons ont disparu et le compartiment est plein.

Dans la pratique, le débit de données maximal théorique sur un intervalle égal à la fenêtre de mémoire tampon n’est jamais atteint. L’exemple précédent supposait une vitesse de données constante. À partir du même compartiment de 3 litres, vous pouvez augmenter le débit de l’emboîtement à 6 litres par minute pendant une minute, puis désactiver l’emboîtement pendant deux minutes. Même si la quantité totale d’eau placée dans le compartiment est comprise dans la valeur théorique maximale de la fenêtre tampon, la concentration de cette valeur dans une partie de la fenêtre provoque un dépassement de capacité du compartiment. À 6 litres par minute, le compartiment à 3 litres déborde peu de temps après 30 secondes. Par conséquent, la quantité maximale réelle de données qui peut être remise à la mémoire tampon sur la durée d’un intervalle égal au paramètre de la fenêtre tampon dépend de la taille des échantillons individuels et de la date de livraison.

Jusqu’à présent, les exemples ont uniquement abordé la mémoire tampon utilisée par le décodeur, mais une mémoire tampon de compartiment perdue est également utilisée par l’encodeur qui crée le contenu compressé. L’encodeur effectue les ajustements nécessaires aux algorithmes de compression pour conserver la vitesse de transmission des échantillons compressés dans les limites décrites par la fenêtre de mémoire tampon et la vitesse de transmission, en supposant que les exemples seront remis au décodeur à une vitesse constante. Vous pouvez considérer le compartiment d’encodeur comme une mise en miroir du compartiment décodeur. Le compartiment de l’encodeur est rempli à un débit variable déterminé par la taille des échantillons individuels et des fuites à une vitesse constante égale à la vitesse de transmission moyenne.

Prenons l’exemple suivant d’un encodeur et d’un décodeur connectés ensemble sur un réseau. Vous encodez un fichier vidéo à 30 images par seconde avec une vitesse de transmission de 6 000 bits par seconde et une fenêtre tampon de 3 secondes (taille totale de la mémoire tampon de 18 000 bits). Le premier échantillon est encodé sous la forme d’une image clé et occupe 7 000 bits. La mémoire tampon de l’encodeur contient désormais 7 000 bits. Les 29 images suivantes sont toutes des images Delta qui totalisent 3 000 bits. Par conséquent, la première seconde de contenu (30 frames) placerait la saturation de la mémoire tampon à 10 000 bits si rien ne se produisait. Nous savons que la vitesse de transmission du flux est de 6 000 bits par seconde. par conséquent, une fois que la première seconde du contenu encodé est placée dans la mémoire tampon de l’encodeur, l’intégralité chute à 4 000 bits. Dans l’application de décodage, ce flux est remis à la mémoire tampon du décodeur à 6 000 bits par seconde. Après une seconde, la mémoire tampon contient 6 000 bits. Le premier exemple contient 7 000 bits, de sorte que la mémoire tampon du décodeur doit être remplie plus avant que le décodeur commence à supprimer des échantillons.

## <a name="setting-leaky-bucket-values-for-asf-streams"></a>Définition des valeurs de compartiment fuites pour les flux ASF

Dans un scénario d’encodage de fichiers, une application peut définir les valeurs de compartiment avec fuites lors de la configuration des flux dans le [Profil ASF](asf-profile.md).

Une fois que vous avez créé le flux et que vous avez une référence à l’interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) du flux, vous pouvez définir les valeurs à l’aide des attributs suivants :

-   [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (valeurs de compartiment de fuite moyenne)
-   [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (valeurs de compartiment à fuites maximales)

Pour plus d’informations sur l’ajout de flux et l’obtention du pointeur **IMFASFStreamConfig** , consultez [Ajout d’informations de flux au récepteur de fichiers ASF](adding-stream-information-to-the-asf-file-sink.md).

Ces valeurs contiennent les informations suivantes :

-   Vitesse de transmission moyenne : obtient la vitesse de transmission moyenne à partir du type de média de sortie sélectionné lors de la négociation de type de média. Utilisez l' [**attribut \_ \_ \_ nombre moyen d' \_ octets \_ par \_ seconde du son**](mf-mt-audio-avg-bytes-per-second-attribute.md) (pour les flux audio) ou l’attribut de [**vitesse de \_ \_ \_ transmission moyenne MF MT**](mf-mt-avg-bitrate-attribute.md) (pour les flux vidéo).
-   Fenêtre de mémoire tampon : Si vous avez une instance de l’encodeur et que vous avez négocié des types de médias de sortie, vous pouvez mettre à jour cette valeur ultérieurement en interrogeant l’encodeur pour l’interface [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) , puis en appelant [**IWMCodecLeakyBucket :: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces. h, wmcodecdspuuid. lib). Dans le cas contraire, utilisez la valeur par défaut de 3000 millisecondes.
-   Taille de la mémoire tampon initiale : définie sur 0.

Les valeurs fournies par l’application dépendent du type d’encodage et du type de média du flux. Par exemple, l' [encodage à vitesse de transmission constante](constant-bit-rate-encoding.md) requiert une vitesse de transmission fixe prédéterminée et une fenêtre de mémoire tampon. L’application peut spécifier ces valeurs de compartiment avec fuites en définissant la propriété de codage [**MFPKEY \_ VIDEOWINDOW**](mfpkey-videowindowproperty.md) et l’attribut [**\_ \_ LEAKYBUCKET1 ASFSTREAMCONFIG MF**](mf-asfstreamconfig-leakybucket1-attribute.md) sur le flux. Les valeurs de fenêtre de mémoire tampon spécifiées sont utilisées pour s’assurer que le fichier encodé a les heures d’envoi correctes marquées sur les paquets de données et que la valeur de préroll s’affiche dans l’objet d’en-tête ASF. Il suffit de définir **MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1** , car ces valeurs spécifiées sont copiées dans l’attribut [**\_ \_ LEAKYBUCKET2 de ASFSTREAMCONFIG MF**](mf-asfstreamconfig-leakybucket2-attribute.md) .

Pour les modes d’encodage à 2 passes, vous devez définir ces deux attributs pour spécifier les valeurs moyennes et maximales.

Pour l’encodage VBR, l’application peut interroger les valeurs de compartiment perdues utilisées par l’encodeur uniquement une fois le test d’encodage terminé. Par conséquent, lors de la configuration du récepteur multimédia, l’application peut choisir de ne pas définir les attributs ou les propriétés liés aux compartiments perdus. Après l’encodage, l’application doit interroger l’encodeur pour les propriétés [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md), [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md), [**MFPKEY \_ Rmax**](mfpkey-rmaxproperty.md)et [**MFPKEY \_**](mfpkey-bmaxproperty.md) BMAX et les définir dans le récepteur multimédia afin que les valeurs exactes soient reflétées dans l’objet d’en-tête. Pour obtenir un exemple de code sur la façon de mettre à jour les valeurs pour l’encodage VBR, consultez « mettre à jour les propriétés d’encodage dans le récepteur de fichiers » dans le [Didacticiel : 1-passer l’encodage Windows Media](tutorial--1-pass-windows-media-encoding.md).

Si vous copiez du contenu Windows Media de la source vers le récepteur multimédia sans encodage, les valeurs des compartiments de fuites doivent être définies dans le récepteur multimédia.

## <a name="leaky-bucket-values-in-the-asf-multiplexer"></a>Valeurs de compartiment avec fuite dans le multiplexeur ASF

Dans Media Foundation, les valeurs de compartiment perdues sont utilisées par le [multiplexeur ASF](asf-multiplexer.md) pour configurer les valeurs de compartiment de fuites internes qu’il utilise pour générer des paquets de données. La charge utile est contenue dans un exemple de média et une série d’exemples de médias constitue un paquet de données ASF. En fonction des valeurs de compartiment perdues et de l’heure de présentation, le multiplexeur attribue un délai d’envoi pour chaque échantillon de support afin que les débits binaires des paquets envoyés sur le réseau soient à une vitesse de transmission constante (*R*).

Une application ne peut pas définir directement de valeurs de compartiment fuites dans le multiplexeur. Les valeurs doivent être fournies sur le récepteur multimédia ASF, qui définit les valeurs appropriées sur le multiplexeur. Les valeurs définies dans les modèles [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) et [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) sont utilisées par le multiplexeur pour valider les exemples envoyés au récepteur multimédia ASF sont générés à l’aide des valeurs spécifiées.

## <a name="updating-leaky-bucket-values-in-the-asf-media-sink"></a>Mise à jour des valeurs de compartiment avec fuite dans le récepteur de média ASF

Une application peut remplacer les valeurs de compartiment avec fuite au niveau du flux (définies dans le profil ASF lors de la création du flux) en définissant la propriété [**MFPKEY \_ ASFSTREAMSINK \_ corrigé \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) dans la Banque de propriétés du récepteur multimédia. Pour obtenir une référence à la Banque de propriétés, utilisez l’objet ContentInfo implémenté par le récepteur multimédia. Pour plus d’informations, consultez [définition des propriétés dans le récepteur de fichiers](setting-properties-in-the-file-sink.md).

**Remarque**  Cette opération est autorisée uniquement pour les flux audio.

Cette propriété doit être définie après que vous avez défini le type de sortie sur l’encodeur. En fonction de la vitesse de transmission définie dans le type de média, l’encodeur calcule la taille de la mémoire tampon pour s’assurer que les exemples de supports générés ne dépassent jamais la mémoire tampon. L’encodeur effectue des ajustements nécessaires pendant la compression pour conserver la vitesse de transmission des échantillons compressés dans les limites décrites par la vitesse de transmission et la fenêtre de mémoire tampon.

À l’instar des attributs de configuration de flux pour les compartiments avec fuite, définissez la vitesse de transmission moyenne et la taille de la mémoire tampon, ainsi que la saturation de la mémoire tampon initiale dans un tableau de DWORDs. Pour plus d’informations, consultez la section « Définition des valeurs des compartiments de fuites pour les flux ASF » dans cette rubrique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Codecs Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 
