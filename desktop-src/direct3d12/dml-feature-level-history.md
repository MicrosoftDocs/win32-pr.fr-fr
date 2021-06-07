---
title: Historique des niveaux de fonctionnalité DirectML
description: TBD
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 1e5d9f8b0532b809bab617655694af68ba530430
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521204"
---
# <a name="directml-feature-level-history"></a><span data-ttu-id="e63d6-103">Historique des niveaux de fonctionnalité DirectML</span><span class="sxs-lookup"><span data-stu-id="e63d6-103">DirectML feature level history</span></span>

<span data-ttu-id="e63d6-104">Pour un historique général des versions de DirectML, consultez [l’historique des versions DirectML](./dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="e63d6-104">For general DirectML version history, see [DirectML version history](./dml-version-history.md).</span></span>

## <a name="dml_feature_level_3_1"></a><span data-ttu-id="e63d6-105">DML_FEATURE_LEVEL_3_1</span><span class="sxs-lookup"><span data-stu-id="e63d6-105">DML_FEATURE_LEVEL_3_1</span></span>

<span data-ttu-id="e63d6-106">Introduit dans DirectML version 1.5.0.</span><span class="sxs-lookup"><span data-stu-id="e63d6-106">Introduced in DirectML version 1.5.0.</span></span>

<span data-ttu-id="e63d6-107">Ajout de la prise en charge des [opérateurs](/windows/win32/api/directml/ne-directml-dml_operator_type)suivants.</span><span class="sxs-lookup"><span data-stu-id="e63d6-107">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="e63d6-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span><span class="sxs-lookup"><span data-stu-id="e63d6-108">**DML_OPERATOR_ELEMENT_WISE_ATAN_YX**</span></span>
* <span data-ttu-id="e63d6-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span><span class="sxs-lookup"><span data-stu-id="e63d6-109">**DML_OPERATOR_ELEMENT_WISE_CLIP_GRAD**</span></span>
* <span data-ttu-id="e63d6-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span><span class="sxs-lookup"><span data-stu-id="e63d6-110">**DML_OPERATOR_ELEMENT_WISE_DIFFERENCE_SQUARE**</span></span>
* <span data-ttu-id="e63d6-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="e63d6-111">**DML_OPERATOR_LOCAL_RESPONSE_NORMALIZATION_GRAD**</span></span>
* <span data-ttu-id="e63d6-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span><span class="sxs-lookup"><span data-stu-id="e63d6-112">**DML_OPERATOR_CUMULATIVE_PRODUCT**</span></span>
* <span data-ttu-id="e63d6-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span><span class="sxs-lookup"><span data-stu-id="e63d6-113">**DML_OPERATOR_BATCH_NORMALIZATION_GRAD**</span></span>

<span data-ttu-id="e63d6-114">Le nombre maximal de dimensions prises en charge pour les opérateurs suivants est passé de 4 à 8.</span><span class="sxs-lookup"><span data-stu-id="e63d6-114">The maximum number of supported dimensions for the following operators has increased from 4 to 8.</span></span>

* <span data-ttu-id="e63d6-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="e63d6-115">**DML_OPERATOR_BATCH_NORMALIZATION**</span></span>
* <span data-ttu-id="e63d6-116">**DML_OPERATOR_CAST**</span><span class="sxs-lookup"><span data-stu-id="e63d6-116">**DML_OPERATOR_CAST**</span></span>
* <span data-ttu-id="e63d6-117">**DML_OPERATOR_JOIN**</span><span class="sxs-lookup"><span data-stu-id="e63d6-117">**DML_OPERATOR_JOIN**</span></span>
* <span data-ttu-id="e63d6-118">**DML_OPERATOR_LP_NORMALIZATION**</span><span class="sxs-lookup"><span data-stu-id="e63d6-118">**DML_OPERATOR_LP_NORMALIZATION**</span></span>
* <span data-ttu-id="e63d6-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="e63d6-119">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="e63d6-120">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="e63d6-120">**DML_OPERATOR_PADDING**</span></span>
* <span data-ttu-id="e63d6-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="e63d6-121">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="e63d6-122">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="e63d6-122">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="e63d6-123">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="e63d6-123">**DML_OPERATOR_TILE**</span></span>
* <span data-ttu-id="e63d6-124">**DML_OPERATOR_TOP_K**</span><span class="sxs-lookup"><span data-stu-id="e63d6-124">**DML_OPERATOR_TOP_K**</span></span>
* <span data-ttu-id="e63d6-125">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="e63d6-125">**DML_OPERATOR_TOP_K1**</span></span>

## <a name="dml_feature_level_3_0"></a><span data-ttu-id="e63d6-126">DML_FEATURE_LEVEL_3_0</span><span class="sxs-lookup"><span data-stu-id="e63d6-126">DML_FEATURE_LEVEL_3_0</span></span>

<span data-ttu-id="e63d6-127">Introduit dans DirectML version 1.4.0.</span><span class="sxs-lookup"><span data-stu-id="e63d6-127">Introduced in DirectML version 1.4.0.</span></span>

<span data-ttu-id="e63d6-128">Ajout de la prise en charge des [opérateurs](/windows/win32/api/directml/ne-directml-dml_operator_type)suivants.</span><span class="sxs-lookup"><span data-stu-id="e63d6-128">Added support for the following [operators](/windows/win32/api/directml/ne-directml-dml_operator_type).</span></span>

* <span data-ttu-id="e63d6-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span><span class="sxs-lookup"><span data-stu-id="e63d6-129">**DML_OPERATOR_ELEMENT_WISE_BIT_AND**</span></span>
* <span data-ttu-id="e63d6-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span><span class="sxs-lookup"><span data-stu-id="e63d6-130">**DML_OPERATOR_ELEMENT_WISE_BIT_OR**</span></span>
* <span data-ttu-id="e63d6-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span><span class="sxs-lookup"><span data-stu-id="e63d6-131">**DML_OPERATOR_ELEMENT_WISE_BIT_XOR**</span></span>
* <span data-ttu-id="e63d6-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span><span class="sxs-lookup"><span data-stu-id="e63d6-132">**DML_OPERATOR_ELEMENT_WISE_BIT_NOT**</span></span>
* <span data-ttu-id="e63d6-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span><span class="sxs-lookup"><span data-stu-id="e63d6-133">**DML_OPERATOR_ELEMENT_WISE_BIT_COUNT**</span></span>
* <span data-ttu-id="e63d6-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="e63d6-134">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="e63d6-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span><span class="sxs-lookup"><span data-stu-id="e63d6-135">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL**</span></span>
* <span data-ttu-id="e63d6-136">**DML_OPERATOR_ACTIVATION_CELU**</span><span class="sxs-lookup"><span data-stu-id="e63d6-136">**DML_OPERATOR_ACTIVATION_CELU**</span></span>
* <span data-ttu-id="e63d6-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span><span class="sxs-lookup"><span data-stu-id="e63d6-137">**DML_OPERATOR_ACTIVATION_RELU_GRAD**</span></span>
* <span data-ttu-id="e63d6-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="e63d6-138">**DML_OPERATOR_AVERAGE_POOLING_GRAD**</span></span>
* <span data-ttu-id="e63d6-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span><span class="sxs-lookup"><span data-stu-id="e63d6-139">**DML_OPERATOR_MAX_POOLING_GRAD**</span></span>
* <span data-ttu-id="e63d6-140">**DML_OPERATOR_RANDOM_GENERATOR**</span><span class="sxs-lookup"><span data-stu-id="e63d6-140">**DML_OPERATOR_RANDOM_GENERATOR**</span></span>
* <span data-ttu-id="e63d6-141">**DML_OPERATOR_NONZERO_COORDINATES**</span><span class="sxs-lookup"><span data-stu-id="e63d6-141">**DML_OPERATOR_NONZERO_COORDINATES**</span></span>
* <span data-ttu-id="e63d6-142">**DML_OPERATOR_RESAMPLE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="e63d6-142">**DML_OPERATOR_RESAMPLE_GRAD**</span></span>
* <span data-ttu-id="e63d6-143">**DML_OPERATOR_SLICE_GRAD**</span><span class="sxs-lookup"><span data-stu-id="e63d6-143">**DML_OPERATOR_SLICE_GRAD**</span></span>
* <span data-ttu-id="e63d6-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span><span class="sxs-lookup"><span data-stu-id="e63d6-144">**DML_OPERATOR_ADAM_OPTIMIZER**</span></span>
* <span data-ttu-id="e63d6-145">**DML_OPERATOR_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="e63d6-145">**DML_OPERATOR_ARGMIN**</span></span>
* <span data-ttu-id="e63d6-146">**DML_OPERATOR_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="e63d6-146">**DML_OPERATOR_ARGMAX**</span></span>
* <span data-ttu-id="e63d6-147">**DML_OPERATOR_ROI_ALIGN**</span><span class="sxs-lookup"><span data-stu-id="e63d6-147">**DML_OPERATOR_ROI_ALIGN**</span></span>
* <span data-ttu-id="e63d6-148">**DML_OPERATOR_GATHER_ND1**</span><span class="sxs-lookup"><span data-stu-id="e63d6-148">**DML_OPERATOR_GATHER_ND1**</span></span>

<span data-ttu-id="e63d6-149">Ajout des améliorations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e63d6-149">Added the following enhancements.</span></span>

* <span data-ttu-id="e63d6-150">Le nombre maximal de dimensions de tenseur a été augmenté de 5 à 8.</span><span class="sxs-lookup"><span data-stu-id="e63d6-150">The maximum number of tensor dimensions has been increased from 5 to 8.</span></span> <span data-ttu-id="e63d6-151">Consultez [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e63d6-151">See [DML_TENSOR_DIMENSION_COUNT_MAX1](./direct3d-directml-constants.md).</span></span>
* <span data-ttu-id="e63d6-152">Une prise en charge supplémentaire des types de données entiers a été ajoutée aux opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="e63d6-152">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="e63d6-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span><span class="sxs-lookup"><span data-stu-id="e63d6-153">**DML_OPERATOR_ELEMENT_WISE_POW**</span></span>
  * <span data-ttu-id="e63d6-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span><span class="sxs-lookup"><span data-stu-id="e63d6-154">**DML_OPERATOR_ELEMENT_WISE_CONSTANT_POW**</span></span>
  * <span data-ttu-id="e63d6-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1** et **DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="e63d6-155">**DML_OPERATOR_MAX_POOLING**, **DML_OPERATOR_MAX_POOLING1**, and **DML_OPERATOR_MAX_POOLING2**</span></span>
  * <span data-ttu-id="e63d6-156">**DML_OPERATOR_REDUCE**, lors de l’utilisation de **DML_REDUCE_FUNCTION_ARGMIN** ou **DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="e63d6-156">**DML_OPERATOR_REDUCE**, when using **DML_REDUCE_FUNCTION_ARGMIN** or **DML_REDUCE_FUNCTION_ARGMAX**</span></span>
* <span data-ttu-id="e63d6-157">Les types de données 64 bits suivants ont été ajoutés et sont pris en charge par les opérateurs Select.</span><span class="sxs-lookup"><span data-stu-id="e63d6-157">The following 64-bit data types have been added, and are supported by select operators.</span></span>
  * <span data-ttu-id="e63d6-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="e63d6-158">**DML_TENSOR_DATA_TYPE_FLOAT64**</span></span>
  * <span data-ttu-id="e63d6-159">**DML_TENSOR_DATA_TYPE_UINT64**</span><span class="sxs-lookup"><span data-stu-id="e63d6-159">**DML_TENSOR_DATA_TYPE_UINT64**</span></span>
  * <span data-ttu-id="e63d6-160">**DML_TENSOR_DATA_TYPE_INT64**</span><span class="sxs-lookup"><span data-stu-id="e63d6-160">**DML_TENSOR_DATA_TYPE_INT64**</span></span>

<span data-ttu-id="e63d6-161">Fonctionnalités dépréciées.</span><span class="sxs-lookup"><span data-stu-id="e63d6-161">Deprecated functionality.</span></span>

* <span data-ttu-id="e63d6-162">**DML_REDUCE_FUNCTION_ARGMAX** et **DML_REDUCE_FUNCTION_ARGMIN** ont été dépréciés.</span><span class="sxs-lookup"><span data-stu-id="e63d6-162">**DML_REDUCE_FUNCTION_ARGMAX** and **DML_REDUCE_FUNCTION_ARGMIN** have been deprecated.</span></span> <span data-ttu-id="e63d6-163">Il est préférable d’utiliser les opérateurs **DML_OPERATOR_ARGMIN** et **DML_OPERATOR_ARGMAX** autonomes à leur place.</span><span class="sxs-lookup"><span data-stu-id="e63d6-163">You should prefer to use the standalone **DML_OPERATOR_ARGMIN** and **DML_OPERATOR_ARGMAX** operators in their place.</span></span>

## <a name="dml_feature_level_2_1"></a><span data-ttu-id="e63d6-164">DML_FEATURE_LEVEL_2_1</span><span class="sxs-lookup"><span data-stu-id="e63d6-164">DML_FEATURE_LEVEL_2_1</span></span>

<span data-ttu-id="e63d6-165">Introduit dans DirectML version 1.2.0.</span><span class="sxs-lookup"><span data-stu-id="e63d6-165">Introduced in DirectML version 1.2.0.</span></span>

<span data-ttu-id="e63d6-166">Ajout des API suivantes.</span><span class="sxs-lookup"><span data-stu-id="e63d6-166">Added the following APIs.</span></span>

* [<span data-ttu-id="e63d6-167">Interface IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="e63d6-167">IDMLDevice1 interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice1)
* <span data-ttu-id="e63d6-168">Prise en charge des graphiques d’opérateur (consultez [IDMLDevice1 :: CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span><span class="sxs-lookup"><span data-stu-id="e63d6-168">Operator graph support (see [IDMLDevice1::CompileGraph](/windows/win32/api/directml/nf-directml-idmldevice1-compilegraph)</span></span>

<span data-ttu-id="e63d6-169">Ajout de la prise en charge des opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="e63d6-169">Added support for the following operators.</span></span>

* <span data-ttu-id="e63d6-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span><span class="sxs-lookup"><span data-stu-id="e63d6-170">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_LEFT**</span></span>
* <span data-ttu-id="e63d6-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="e63d6-171">**DML_OPERATOR_ELEMENT_WISE_BIT_SHIFT_RIGHT**</span></span>
* <span data-ttu-id="e63d6-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span><span class="sxs-lookup"><span data-stu-id="e63d6-172">**DML_OPERATOR_ELEMENT_WISE_ROUND**</span></span>
* <span data-ttu-id="e63d6-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span><span class="sxs-lookup"><span data-stu-id="e63d6-173">**DML_OPERATOR_ELEMENT_WISE_IS_INFINITY**</span></span>
* <span data-ttu-id="e63d6-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span><span class="sxs-lookup"><span data-stu-id="e63d6-174">**DML_OPERATOR_ELEMENT_WISE_MODULUS_TRUNCATE**</span></span>
* <span data-ttu-id="e63d6-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span><span class="sxs-lookup"><span data-stu-id="e63d6-175">**DML_OPERATOR_ELEMENT_WISE_MODULUS_FLOOR**</span></span>
* <span data-ttu-id="e63d6-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span><span class="sxs-lookup"><span data-stu-id="e63d6-176">**DML_OPERATOR_FILL_VALUE_CONSTANT**</span></span>
* <span data-ttu-id="e63d6-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span><span class="sxs-lookup"><span data-stu-id="e63d6-177">**DML_OPERATOR_FILL_VALUE_SEQUENCE**</span></span>
* <span data-ttu-id="e63d6-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span><span class="sxs-lookup"><span data-stu-id="e63d6-178">**DML_OPERATOR_CUMULATIVE_SUMMATION**</span></span>
* <span data-ttu-id="e63d6-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span><span class="sxs-lookup"><span data-stu-id="e63d6-179">**DML_OPERATOR_REVERSE_SUBSEQUENCES**</span></span>
* <span data-ttu-id="e63d6-180">**DML_OPERATOR_GATHER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="e63d6-180">**DML_OPERATOR_GATHER_ELEMENTS**</span></span>
* <span data-ttu-id="e63d6-181">**DML_OPERATOR_GATHER_ND**</span><span class="sxs-lookup"><span data-stu-id="e63d6-181">**DML_OPERATOR_GATHER_ND**</span></span>
* <span data-ttu-id="e63d6-182">**DML_OPERATOR_SCATTER_ND**</span><span class="sxs-lookup"><span data-stu-id="e63d6-182">**DML_OPERATOR_SCATTER_ND**</span></span>
* <span data-ttu-id="e63d6-183">**DML_OPERATOR_MAX_POOLING2**</span><span class="sxs-lookup"><span data-stu-id="e63d6-183">**DML_OPERATOR_MAX_POOLING2**</span></span>
* <span data-ttu-id="e63d6-184">**DML_OPERATOR_SLICE1**</span><span class="sxs-lookup"><span data-stu-id="e63d6-184">**DML_OPERATOR_SLICE1**</span></span>
* <span data-ttu-id="e63d6-185">**DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="e63d6-185">**DML_OPERATOR_TOP_K1**</span></span>
* <span data-ttu-id="e63d6-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span><span class="sxs-lookup"><span data-stu-id="e63d6-186">**DML_OPERATOR_DEPTH_TO_SPACE1**</span></span>
* <span data-ttu-id="e63d6-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span><span class="sxs-lookup"><span data-stu-id="e63d6-187">**DML_OPERATOR_SPACE_TO_DEPTH1**</span></span>
* <span data-ttu-id="e63d6-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span><span class="sxs-lookup"><span data-stu-id="e63d6-188">**DML_OPERATOR_MEAN_VARIANCE_NORMALIZATION1**</span></span>
* <span data-ttu-id="e63d6-189">**DML_OPERATOR_RESAMPLE1**</span><span class="sxs-lookup"><span data-stu-id="e63d6-189">**DML_OPERATOR_RESAMPLE1**</span></span>
* <span data-ttu-id="e63d6-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="e63d6-190">**DML_OPERATOR_MATRIX_MULTIPLY_INTEGER**</span></span>
* <span data-ttu-id="e63d6-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="e63d6-191">**DML_OPERATOR_QUANTIZED_LINEAR_MATRIX_MULTIPLY**</span></span>
* <span data-ttu-id="e63d6-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span><span class="sxs-lookup"><span data-stu-id="e63d6-192">**DML_OPERATOR_CONVOLUTION_INTEGER**</span></span>
* <span data-ttu-id="e63d6-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span><span class="sxs-lookup"><span data-stu-id="e63d6-193">**DML_OPERATOR_QUANTIZED_LINEAR_CONVOLUTION**</span></span>

<span data-ttu-id="e63d6-194">Ajout des améliorations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e63d6-194">Added the following enhancements.</span></span>

* <span data-ttu-id="e63d6-195">Une prise en charge supplémentaire des types de données entiers a été ajoutée aux opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="e63d6-195">Additional support for integer datatypes has been added to the following operators.</span></span>
  * <span data-ttu-id="e63d6-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span><span class="sxs-lookup"><span data-stu-id="e63d6-196">**DML_OPERATOR_ELEMENT_WISE_IDENTITY**</span></span>
  * <span data-ttu-id="e63d6-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span><span class="sxs-lookup"><span data-stu-id="e63d6-197">**DML_OPERATOR_ELEMENT_WISE_ABS**</span></span>
  * <span data-ttu-id="e63d6-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span><span class="sxs-lookup"><span data-stu-id="e63d6-198">**DML_OPERATOR_ELEMENT_WISE_ADD**</span></span>
  * <span data-ttu-id="e63d6-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span><span class="sxs-lookup"><span data-stu-id="e63d6-199">**DML_OPERATOR_ELEMENT_WISE_CLIP**</span></span>
  * <span data-ttu-id="e63d6-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span><span class="sxs-lookup"><span data-stu-id="e63d6-200">**DML_OPERATOR_ELEMENT_WISE_DIVIDE**</span></span>
  * <span data-ttu-id="e63d6-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="e63d6-201">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="e63d6-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="e63d6-202">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="e63d6-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="e63d6-203">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="e63d6-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span><span class="sxs-lookup"><span data-stu-id="e63d6-204">**DML_OPERATOR_ELEMENT_WISE_MAX**</span></span>
  * <span data-ttu-id="e63d6-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span><span class="sxs-lookup"><span data-stu-id="e63d6-205">**DML_OPERATOR_ELEMENT_WISE_MEAN**</span></span>
  * <span data-ttu-id="e63d6-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span><span class="sxs-lookup"><span data-stu-id="e63d6-206">**DML_OPERATOR_ELEMENT_WISE_MIN**</span></span>
  * <span data-ttu-id="e63d6-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="e63d6-207">**DML_OPERATOR_ELEMENT_WISE_MULTIPLY**</span></span>
  * <span data-ttu-id="e63d6-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="e63d6-208">**DML_OPERATOR_ELEMENT_WISE_SUBTRACT**</span></span>
  * <span data-ttu-id="e63d6-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span><span class="sxs-lookup"><span data-stu-id="e63d6-209">**DML_OPERATOR_ELEMENT_WISE_THRESHOLD**</span></span>
  * <span data-ttu-id="e63d6-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="e63d6-210">**DML_OPERATOR_ELEMENT_WISE_QUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="e63d6-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span><span class="sxs-lookup"><span data-stu-id="e63d6-211">**DML_OPERATOR_ELEMENT_WISE_DEQUANTIZE_LINEAR**</span></span>
  * <span data-ttu-id="e63d6-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="e63d6-212">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
  * <span data-ttu-id="e63d6-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="e63d6-213">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
  * <span data-ttu-id="e63d6-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="e63d6-214">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
  * <span data-ttu-id="e63d6-215">**DML_OPERATOR_PADDING**</span><span class="sxs-lookup"><span data-stu-id="e63d6-215">**DML_OPERATOR_PADDING**</span></span>
  * <span data-ttu-id="e63d6-216">**DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="e63d6-216">**DML_OPERATOR_GATHER**</span></span>
  * <span data-ttu-id="e63d6-217">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="e63d6-217">**DML_OPERATOR_SCATTER**</span></span>
  * <span data-ttu-id="e63d6-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span><span class="sxs-lookup"><span data-stu-id="e63d6-218">**DML_OPERATOR_DEPTH_TO_SPACE**</span></span>
  * <span data-ttu-id="e63d6-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span><span class="sxs-lookup"><span data-stu-id="e63d6-219">**DML_OPERATOR_SPACE_TO_DEPTH**</span></span>
  * <span data-ttu-id="e63d6-220">**DML_OPERATOR_TILE**</span><span class="sxs-lookup"><span data-stu-id="e63d6-220">**DML_OPERATOR_TILE**</span></span>
  * <span data-ttu-id="e63d6-221">**DML_OPERATOR_TOP_K** et **DML_OPERATOR_TOP_K1**</span><span class="sxs-lookup"><span data-stu-id="e63d6-221">**DML_OPERATOR_TOP_K** and **DML_OPERATOR_TOP_K1**</span></span>
  * <span data-ttu-id="e63d6-222">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="e63d6-222">**DML_OPERATOR_ONE_HOT**</span></span>
  * <span data-ttu-id="e63d6-223">**DML_OPERATOR_REDUCE**, lors de l’utilisation de l’une des fonctions de réduction suivantes.</span><span class="sxs-lookup"><span data-stu-id="e63d6-223">**DML_OPERATOR_REDUCE**, when using one of the following reduce functions.</span></span>
    * <span data-ttu-id="e63d6-224">**DML_REDUCE_FUNCTION_ARGMIN**</span><span class="sxs-lookup"><span data-stu-id="e63d6-224">**DML_REDUCE_FUNCTION_ARGMIN**</span></span>
    * <span data-ttu-id="e63d6-225">**DML_REDUCE_FUNCTION_ARGMAX**</span><span class="sxs-lookup"><span data-stu-id="e63d6-225">**DML_REDUCE_FUNCTION_ARGMAX**</span></span>
    * <span data-ttu-id="e63d6-226">**DML_REDUCE_FUNCTION_MAX**</span><span class="sxs-lookup"><span data-stu-id="e63d6-226">**DML_REDUCE_FUNCTION_MAX**</span></span>
    * <span data-ttu-id="e63d6-227">**DML_REDUCE_FUNCTION_MIN**</span><span class="sxs-lookup"><span data-stu-id="e63d6-227">**DML_REDUCE_FUNCTION_MIN**</span></span>
    * <span data-ttu-id="e63d6-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span><span class="sxs-lookup"><span data-stu-id="e63d6-228">**DML_REDUCE_FUNCTION_MULTIPLY**</span></span>
    * <span data-ttu-id="e63d6-229">**DML_REDUCE_FUNCTION_SUM**</span><span class="sxs-lookup"><span data-stu-id="e63d6-229">**DML_REDUCE_FUNCTION_SUM**</span></span>
* <span data-ttu-id="e63d6-230">Restrictions de forme de tenseur souple pour **DML_OPERATOR_GATHER**</span><span class="sxs-lookup"><span data-stu-id="e63d6-230">Relaxed tensor shape restrictions for **DML_OPERATOR_GATHER**</span></span>

## <a name="dml_feature_level_2_0"></a><span data-ttu-id="e63d6-231">DML_FEATURE_LEVEL_2_0</span><span class="sxs-lookup"><span data-stu-id="e63d6-231">DML_FEATURE_LEVEL_2_0</span></span>

<span data-ttu-id="e63d6-232">Introduit dans DirectML version 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="e63d6-232">Introduced in DirectML version 1.1.0.</span></span>

<span data-ttu-id="e63d6-233">Ajout des API suivantes.</span><span class="sxs-lookup"><span data-stu-id="e63d6-233">Added the following APIs.</span></span>
* [<span data-ttu-id="e63d6-234">Fonction DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="e63d6-234">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [<span data-ttu-id="e63d6-235">Énumération DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="e63d6-235">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* <span data-ttu-id="e63d6-236">Requêtes au niveau des fonctionnalités (voir [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span><span class="sxs-lookup"><span data-stu-id="e63d6-236">Feature level queries (see [DML_FEATURE_QUERY_FEATURE_LEVELS](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels))</span></span>

<span data-ttu-id="e63d6-237">Ajout de la prise en charge des opérateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="e63d6-237">Added support for the following operators.</span></span>

* <span data-ttu-id="e63d6-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span><span class="sxs-lookup"><span data-stu-id="e63d6-238">**DML_OPERATOR_ELEMENT_WISE_SIGN**</span></span>
* <span data-ttu-id="e63d6-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span><span class="sxs-lookup"><span data-stu-id="e63d6-239">**DML_OPERATOR_ELEMENT_WISE_IS_NAN**</span></span>
* <span data-ttu-id="e63d6-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span><span class="sxs-lookup"><span data-stu-id="e63d6-240">**DML_OPERATOR_ELEMENT_WISE_ERF**</span></span>
* <span data-ttu-id="e63d6-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span><span class="sxs-lookup"><span data-stu-id="e63d6-241">**DML_OPERATOR_ELEMENT_WISE_SINH**</span></span>
* <span data-ttu-id="e63d6-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span><span class="sxs-lookup"><span data-stu-id="e63d6-242">**DML_OPERATOR_ELEMENT_WISE_COSH**</span></span>
* <span data-ttu-id="e63d6-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span><span class="sxs-lookup"><span data-stu-id="e63d6-243">**DML_OPERATOR_ELEMENT_WISE_TANH**</span></span>
* <span data-ttu-id="e63d6-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span><span class="sxs-lookup"><span data-stu-id="e63d6-244">**DML_OPERATOR_ELEMENT_WISE_ASINH**</span></span>
* <span data-ttu-id="e63d6-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span><span class="sxs-lookup"><span data-stu-id="e63d6-245">**DML_OPERATOR_ELEMENT_WISE_ACOSH**</span></span>
* <span data-ttu-id="e63d6-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span><span class="sxs-lookup"><span data-stu-id="e63d6-246">**DML_OPERATOR_ELEMENT_WISE_ATANH**</span></span>
* <span data-ttu-id="e63d6-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span><span class="sxs-lookup"><span data-stu-id="e63d6-247">**DML_OPERATOR_ELEMENT_WISE_IF**</span></span>
* <span data-ttu-id="e63d6-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span><span class="sxs-lookup"><span data-stu-id="e63d6-248">**DML_OPERATOR_ELEMENT_WISE_ADD1**</span></span>
* <span data-ttu-id="e63d6-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span><span class="sxs-lookup"><span data-stu-id="e63d6-249">**DML_OPERATOR_ACTIVATION_SHRINK**</span></span>
* <span data-ttu-id="e63d6-250">**DML_OPERATOR_MAX_POOLING1**</span><span class="sxs-lookup"><span data-stu-id="e63d6-250">**DML_OPERATOR_MAX_POOLING1**</span></span>
* <span data-ttu-id="e63d6-251">**DML_OPERATOR_MAX_UNPOOLING**</span><span class="sxs-lookup"><span data-stu-id="e63d6-251">**DML_OPERATOR_MAX_UNPOOLING**</span></span>
* <span data-ttu-id="e63d6-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span><span class="sxs-lookup"><span data-stu-id="e63d6-252">**DML_OPERATOR_DIAGONAL_MATRIX**</span></span>
* <span data-ttu-id="e63d6-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span><span class="sxs-lookup"><span data-stu-id="e63d6-253">**DML_OPERATOR_SCATTER_ELEMENTS**</span></span>
* <span data-ttu-id="e63d6-254">**DML_OPERATOR_SCATTER**</span><span class="sxs-lookup"><span data-stu-id="e63d6-254">**DML_OPERATOR_SCATTER**</span></span>
* <span data-ttu-id="e63d6-255">**DML_OPERATOR_ONE_HOT**</span><span class="sxs-lookup"><span data-stu-id="e63d6-255">**DML_OPERATOR_ONE_HOT**</span></span>
* <span data-ttu-id="e63d6-256">**DML_OPERATOR_RESAMPLE**</span><span class="sxs-lookup"><span data-stu-id="e63d6-256">**DML_OPERATOR_RESAMPLE**</span></span>

<span data-ttu-id="e63d6-257">Ajout des améliorations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e63d6-257">Added the following enhancements.</span></span>

* <span data-ttu-id="e63d6-258">Lors de la liaison d’une ressource d’entrée pour la distribution d’un [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), il est maintenant légal de fournir une ressource avec [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (en plus de **D3D12_HEAP_TYPE_DEFAULT**), à condition que les propriétés de tas appropriées soient également définies.</span><span class="sxs-lookup"><span data-stu-id="e63d6-258">When binding an input resource for dispatch of an [IDMLOperatorInitializer](/windows/win32/api/directml/nn-directml-idmloperatorinitializer), it's now legal to provide a resource with [D3D12_HEAP_TYPE_CUSTOM](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type) (in addition to **D3D12_HEAP_TYPE_DEFAULT**), as long as appropriate heap properties are also set.</span></span> <span data-ttu-id="e63d6-259">Consultez [liaison dans DirectML](./dml-binding.md).</span><span class="sxs-lookup"><span data-stu-id="e63d6-259">See [Binding in DirectML](./dml-binding.md).</span></span>
* <span data-ttu-id="e63d6-260">Les opérateurs booléens logiques suivants prennent désormais en charge les dizaines de temps de sortie **UINT8** , en plus de la prise en charge existante de **UInt32**.</span><span class="sxs-lookup"><span data-stu-id="e63d6-260">The following logical boolean operators now support **UINT8** output tensors, in addition to the existing support for **UINT32**.</span></span>
  * <span data-ttu-id="e63d6-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span><span class="sxs-lookup"><span data-stu-id="e63d6-261">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_AND**</span></span>
  * <span data-ttu-id="e63d6-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span><span class="sxs-lookup"><span data-stu-id="e63d6-262">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_EQUALS**</span></span>
  * <span data-ttu-id="e63d6-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span><span class="sxs-lookup"><span data-stu-id="e63d6-263">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_GREATER_THAN**</span></span>
  * <span data-ttu-id="e63d6-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span><span class="sxs-lookup"><span data-stu-id="e63d6-264">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_LESS_THAN**</span></span>
  * <span data-ttu-id="e63d6-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span><span class="sxs-lookup"><span data-stu-id="e63d6-265">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_NOT**</span></span>
  * <span data-ttu-id="e63d6-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span><span class="sxs-lookup"><span data-stu-id="e63d6-266">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_OR**</span></span>
  * <span data-ttu-id="e63d6-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span><span class="sxs-lookup"><span data-stu-id="e63d6-267">**DML_OPERATOR_ELEMENT_WISE_LOGICAL_XOR**</span></span>
* <span data-ttu-id="e63d6-268">5J les fonctions d’activation prennent désormais en charge l’utilisation de Strides sur leurs dizaines d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="e63d6-268">5D activation functions now support the use of strides on their input and output tensors.</span></span>

## <a name="dml_feature_level_1_0"></a><span data-ttu-id="e63d6-269">DML_FEATURE_LEVEL_1_0</span><span class="sxs-lookup"><span data-stu-id="e63d6-269">DML_FEATURE_LEVEL_1_0</span></span>

<span data-ttu-id="e63d6-270">Niveau de fonctionnalité dans lequel DirectML a été introduit.</span><span class="sxs-lookup"><span data-stu-id="e63d6-270">The feature level in which DirectML was introduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="e63d6-271">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e63d6-271">See also</span></span>

* [<span data-ttu-id="e63d6-272">Historique des versions DirectML</span><span class="sxs-lookup"><span data-stu-id="e63d6-272">DirectML version history</span></span>](./dml-version-history.md)
* [<span data-ttu-id="e63d6-273">Énumération DML_FEATURE_LEVEL</span><span class="sxs-lookup"><span data-stu-id="e63d6-273">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="e63d6-274">Fonction DMLCreateDevice1</span><span class="sxs-lookup"><span data-stu-id="e63d6-274">DMLCreateDevice1 function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice1.md)
* [<span data-ttu-id="e63d6-275">Structure DML_FEATURE_QUERY_FEATURE_LEVELS</span><span class="sxs-lookup"><span data-stu-id="e63d6-275">DML_FEATURE_QUERY_FEATURE_LEVELS structure</span></span>](/windows/win32/api/directml/ns-directml-dml_feature_query_feature_levels)
